<template>
  <div class="overlay">
    <div v-click-outside="close" class="sidebar">
      <div class="sidebar-content">
        <div @click="close" class="close">
          <close />
        </div>
        <div class="image-wrapper">
          <login />
        </div>
        <span class="heading">Войти с помощью</span>
        <login-button google class="button" />
        <login-button yandex class="button" />
      </div>
    </div>
  </div>
</template>

<script>
import ClickOutside from 'vue-click-outside'

import Close from '~/components/graphic/Close'
import Login from '~/components/graphic/Login'
import LoginButton from '~/components/input/LoginButton'

export default {
  components: {
    Close,
    Login,
    LoginButton
  },

  directives: {
    ClickOutside
  },

  methods: {
    close() {
      this.$emit('closeClicked')
    }
  }
}
</script>

<style lang="scss" scoped>
.overlay {
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  position: fixed;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 1000;

  .sidebar {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    width: 350px;

    .sidebar-content {
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: center;
      height: 100%;
      padding: 42px;
      background: $white;

      .close {
        position: absolute;
        left: 25px;
        top: 30px;
        width: 32px;
        height: 32px;
        transition: $duration opacity;
        cursor: pointer;

        &:hover {
          opacity: $hoverOpacity;
        }
      }

      .image-wrapper {
        display: flex;
        justify-content: center;
        margin: 112px 0 50px;
      }

      .heading {
        font-style: normal;
        font-weight: bold;
        font-size: 25px;
        line-height: 35px;
        margin-bottom: 30px;
      }

      .button {
        width: 100%;
        margin-bottom: 25px;
      }
    }
  }
}
</style>
