<template>
  <button
    :class="{ 'login-button--google': google, 'login-button--yandex': yandex }"
    class="login-button"
  >
    <span class="name">{{ name }}</span>
    <Google v-if="google" />
    <Yandex v-if="yandex" />
  </button>
</template>

<script>
import Google from '~/components/graphic/Google'
import Yandex from '~/components/graphic/Yandex'

export default {
  components: {
    Google,
    Yandex
  },

  props: {
    google: {
      type: Boolean,
      default: false
    },

    yandex: {
      type: Boolean,
      default: false
    }
  },

  computed: {
    name() {
      if (this.google) {
        return 'Google'
      } else if (this.yandex) {
        return 'Яндекс'
      } else return ''
    }
  }
}
</script>

<style lang="scss" scoped>
.login-button {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 50px;
  border-radius: 10px;
  padding: 10px 20px;
  outline: none;
  transition: $duration opacity;
  border: none;
  cursor: pointer;

  &:hover {
    opacity: $hoverOpacity;
  }

  &--google {
    background: #dd4330;
    color: $white;
  }

  &--yandex {
    background: #f6cd46;
    color: $black;
  }

  .name {
    font-style: normal;
    font-weight: 600;
    font-size: 14px;
    line-height: 22px;
  }
}
</style>
