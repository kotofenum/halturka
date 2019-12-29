<template>
  <span class="regular-text"><slot /></span>
</template>

<style lang="scss" scoped>
.regular-text {
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 26px;

  > p:not(:first-of-type) {
    margin-top: 13px;
  }

  > p:not(:last-of-type) {
    margin-bottom: 13px;
  }
}
</style>
