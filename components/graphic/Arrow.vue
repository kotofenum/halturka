<template>
  <svg
    :class="reversed && 'arrow--reversed'"
    width="30"
    height="30"
    viewBox="0 0 30 30"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    class="arrow"
  >
    <path
      d="M25.0195 13.7695V16.2305H9.78516L16.7578 23.2617L15 25.0195L4.98047 15L15 4.98047L16.7578 6.73828L9.78516 13.7695H25.0195Z"
      fill="black"
    />
  </svg>
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
.arrow {
  &--reversed {
    transform: rotate(180deg);
  }
}
</style>
