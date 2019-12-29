<template>
  <page-column class="info-block">
    <lead-heading class="heading"><slot name="heading"/></lead-heading>
    <regular-text class="content">
      <slot name="content" />
    </regular-text>
    <div class="actions">
      <slot name="actions" />
    </div>
  </page-column>
</template>

<script>
import PageColumn from '~/components/layout/PageColumn'
import LeadHeading from '~/components/typeface/LeadHeading'
import RegularText from '~/components/typeface/RegularText'

export default {
  components: {
    PageColumn,
    LeadHeading,
    RegularText
  }
}
</script>

<style lang="scss" scoped>
.info-block {
  .heading {
    margin-bottom: 30px;
  }

  .content {
    margin-bottom: 66px;
  }
  .actions {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 30px;
  }
}
</style>
