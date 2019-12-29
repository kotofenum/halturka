<template>
  <div class="slider-card">
    <div class="heading">
      <span class="step"><slot name="step"/></span>
      <span class="title"><slot name="title"/></span>
    </div>
    <div class="icon">
      <!-- https://github.com/nuxt/eslint-plugin-nuxt/issues/65 -->
      <!-- eslint-disable-next-line vue/require-component-is -->
      <component :is="icon" />
    </div>
    <regular-text>
      <p
        v-html="paragraph"
        v-for="(paragraph, idx) in description"
        :key="idx"
      />
    </regular-text>
  </div>
</template>

<script>
import RegularText from '~/components/typeface/RegularText'

import * as slides from '~/components/graphic/slides'

export default {
  components: {
    RegularText,
    ...slides
  },

  props: {
    icon: {
      type: String,
      required: true
    },

    description: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.slider-card {
  width: 445px;
  height: 600px;
  padding: 50px 60px 30px 60px;
  background: $white;

  .heading {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    height: 70px;

    .step {
      color: $brand;
      margin-right: 16px;

      font-style: normal;
      font-weight: 200;
      font-size: 80px;
    }

    .title {
      color: $black;

      font-style: normal;
      font-weight: 800;
      font-size: 30px;
      line-height: 35px;
    }
  }

  .icon {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 235px;
    margin: 20px 0;
  }
}
</style>
