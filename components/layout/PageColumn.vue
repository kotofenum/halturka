<template>
  <div class="page-column">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.page-column {
  display: flex;
  flex-direction: column;
  color: $darkGray;
}
</style>
