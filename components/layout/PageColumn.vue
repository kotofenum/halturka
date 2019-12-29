<template>
  <div class="page-column">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.page-column {
  display: flex;
  flex-direction: column;
  width: calc(50% - 10px);
  color: $darkGray;
}
</style>
