<template>
  <div :class="lastThree && 'slider--reversed'" class="slider">
    <div v-swiper:mySwiper="swiperOption">
      <div class="swiper-wrapper">
        <slider-card
          v-for="(slide, idx) in slides"
          :key="idx"
          :icon="slide.icon"
          :description="slide.description"
          class="swiper-slide"
        >
          <template slot="step">{{ slide.step }}</template>
          <template slot="title">{{ slide.title }}</template>
        </slider-card>
      </div>
    </div>
    <div class="controller-wrapper">
      <div class="controller">
        <div class="dots" />
        <div class="arrows">
          <arrow class="prev" />
          <arrow class="next" reversed />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SliderCard from '~/components/SliderCard'
import Arrow from '~/components/graphic/Arrow'

import slideData from '~/static/slideData.json'

export default {
  components: {
    SliderCard,
    Arrow
  },

  props: {
    lastThree: {
      type: Boolean,
      default: false
    }
  },

  data() {
    return {
      swiperOption: {
        pagination: {
          el: '.dots',
          clickable: true
        },
        navigation: {
          nextEl: '.next',
          prevEl: '.prev'
        }
      },
      slides: []
    }
  },

  created() {
    const slides = slideData && slideData.slides
    if (slides && slides.length) {
      this.slides = this.lastThree ? slides.slice(-3) : slides.slice(0, 3)
    } else {
      return []
    }
  },

  methods: {
    next() {}
  }
}
</script>

<style lang="scss">
.slider {
  position: relative;

  .swiper-container {
    width: 445px !important;
    margin-left: auto;
    margin-right: 0;
    box-shadow: $boxShadow;
  }
  .swiper-pagination-bullet {
    width: 15px;
    height: 15px;
    border-radius: 50%;
    border: 2px solid $brand;
    background: $brand;
    opacity: 1;
    transition: $duration opacity;
    outline: none;
    cursor: pointer;

    &:hover {
      opacity: $hoverOpacity;
    }

    &-active {
      background: $white;
      pointer-events: none;
    }
  }
  .controller-wrapper {
    position: absolute;
    right: 60px;
    // right: -20px;
    top: 394px;
    z-index: 1;
    pointer-events: none;

    .controller {
      height: 2px;
      width: 505px;
      position: relative;
      background: $brand;
      margin-bottom: 20px;

      .dots {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 75px;
        height: 15px;
        position: absolute;
        left: 20px;
        // right: 20px;
        top: -30px;
        pointer-events: all;
      }

      .arrows {
        display: flex;
        justify-content: space-between;
        width: 85px;
        height: 30px;
        position: absolute;
        left: 15px;
        // right: 15px;
        top: 10px;
        pointer-events: all;

        .prev,
        .next {
          cursor: pointer;
          transition: $duration opacity;

          &:hover {
            opacity: $hoverOpacity;
          }
        }
      }
    }
  }

  &--reversed {
    .swiper-container {
      margin-left: 0;
      margin-right: auto;
    }

    .controller-wrapper {
      right: auto;
      left: 60px;

      .controller {
        .dots {
          left: auto;
          right: 20px;
        }

        .arrows {
          left: auto;
          right: 15px;
        }
      }
    }
  }
}
</style>
