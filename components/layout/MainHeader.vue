<template>
  <div class="main-header">
    <page-content class="content">
      <router-link to="/"><logo /></router-link>
      <button-input
        @click.native.stop="$emit('loginClicked')"
        class="login-button"
        >Войти</button-input
      >
    </page-content>
  </div>
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
  padding: 22px;

  .content {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .login-button {
    height: 40px;
  }
}
</style>
