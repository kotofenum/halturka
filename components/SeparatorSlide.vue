<template>
  <div :class="'separator-slide--type-' + type" class="separator-slide">
    <page-content class="content"><slot /></page-content>
  </div>
</template>

<script>
import PageContent from '~/components/layout/PageContent'

export default {
  components: {
    PageContent
  },

  props: {
    type: {
      type: Number,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.separator-slide {
  color: $brand;
  overflow: hidden;

  font-style: normal;
  font-weight: 600;
  font-size: 30px;
  line-height: 37px;

  &--type-1 {
    background: linear-gradient(
      152.9deg,
      #f8fafb 0%,
      rgba(212, 231, 254, 0.5) 136.35%
    );
  }

  &--type-2 {
    background: linear-gradient(
      258.82deg,
      rgba(158, 190, 241, 0.05) 0.09%,
      rgba(217, 211, 255, 0.4) 99.89%
    );
  }

  .content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 300px;
    padding: 0 100px;
  }
}
</style>
