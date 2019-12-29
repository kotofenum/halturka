<template>
  <div :class="reversed && 'content-slide--reversed'" class="content-slide">
    <slot name="info" />
    <div>
      <slot name="slider" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    reversed: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.content-slide {
  display: flex;
  justify-content: space-between;
  padding: 90px 0;

  &--reversed {
    flex-direction: row-reverse;
  }

  > * {
    width: $halfScreenCalc;
  }
}
</style>
