<template>
  <page-content class="main-header">
    <logo />
    <button-input class="login-button">Войти</button-input>
  </page-content>
</template>

<script>
import PageContent from '~/components/layout/PageContent'
import Logo from '~/components/graphic/Logo'
import ButtonInput from '~/components/input/ButtonInput'

export default {
  components: {
    PageContent,
    Logo,
    ButtonInput
  }
}
</script>

<style lang="scss" scoped>
.main-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 22px 0;
  width: 100%;

  .login-button {
    min-width: 115px;
    height: 40px;
  }
}
</style>
