<template>
  <div class="slider-card">
    <div class="heading">
      <span class="step"><slot name="step"/></span>
      <span class="title">Пополни баланс</span>
    </div>
    <div class="icon" />
    <regular-text>
      <p>Для доступа к системе необходимо положить деньги на свой счет.</p>
      <p>Не волнуйся, это не значит, что ты больше их не увидишь!</p>
    </regular-text>
  </div>
</template>

<script>
import RegularText from '~/components/typeface/RegularText'

// import Arrow from '~/components/graphic/Arrow'

export default {
  components: {
    RegularText
    // Arrow
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
    background: lightgoldenrodyellow;
  }
}
</style>
