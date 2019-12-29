<template>
  <button :class="primary && 'button-input--primary'" class="button-input">
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    primary: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.button-input {
  display: flex;
  align-items: center;
  justify-content: center;
  border: 2px solid $brand;
  box-sizing: border-box;
  border-radius: 10px;
  padding: 0 8px;
  min-width: 115px;
  height: 50px;
  background: $white;
  transition: $duration opacity;
  cursor: pointer;

  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;
  color: $brand;

  outline: none;

  &:hover {
    opacity: $hoverOpacity;
  }

  &--primary {
    background: $red;
    border-color: $red;
    color: $white;
  }
}
</style>
