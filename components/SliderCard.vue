<template>
  <div class="slider-card">
    <div class="heading">
      <span class="step">01</span>
      <span class="title">Пополни баланс</span>
    </div>
    <div class="icon" />
    <div class="controller">
      <div class="dots">
        <div class="dot dot--selected" />
        <div class="dot" />
        <div class="dot" />
      </div>
      <div class="arrows">
        <arrow />
        <arrow reversed />
      </div>
    </div>
    <regular-text>
      <p>Для доступа к системе необходимо положить деньги на свой счет.</p>
      <p>Не волнуйся, это не значит, что ты больше их не увидишь!</p>
    </regular-text>
  </div>
</template>

<script>
import RegularText from '~/components/typeface/RegularText'

import Arrow from '~/components/graphic/Arrow'

export default {
  components: {
    RegularText,
    Arrow
  }
}
</script>

<style lang="scss" scoped>
.slider-card {
  width: 445px;
  height: 600px;
  padding: 50px 60px 30px 60px;
  background: $white;
  box-shadow: $boxShadow;

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
    height: 235px;
    margin: 20px 0;
    background: lightgoldenrodyellow;
  }

  .controller {
    height: 2px;
    width: 505px;
    position: relative;
    right: 180px;
    background: $brand;
    margin-bottom: 20px;

    .dots {
      display: flex;
      justify-content: space-between;
      width: 75px;
      height: 15px;
      position: absolute;
      left: 20px;
      top: -30px;

      .dot {
        width: 15px;
        height: 15px;
        border-radius: 50%;
        border: 2px solid $brand;
        background: $brand;

        &--selected {
          background: $white;
        }
      }
    }

    .arrows {
      display: flex;
      justify-content: space-between;
      width: 85px;
      height: 30px;
      position: absolute;
      left: 15px;
      top: 10px;
    }
  }
}
</style>
