<template>
  <div class="main-footer">
    <page-content class="content">
      <div class="wrapper">
        <router-link to="/"><logo class="logo"/></router-link>
        <div class="info">
          <span class="info-heading">Информация</span>
          <a href="" class="info-link">О нас</a>
          <a href="" class="info-link">Наши методики</a>
          <a href="" class="info-link">Политика конфиденциальности</a>
        </div>
      </div>
      <div class="wrapper">
        <div class="info contact">
          <span class="info-heading">Для связи с нами</span>
          <div class="social-wrapper">
            <a href="http://facebook.com"><facebook class="social"/></a>
            <a href="http://instagram.com"><instagram class="social"/></a>
            <a href="mailto:test@test.com"><email class="social"/></a>
          </div>
        </div>
      </div>
    </page-content>
  </div>
</template>

<script>
import PageContent from '~/components/layout/PageContent'
import Logo from '~/components/graphic/Logo'
import Facebook from '~/components/graphic/Facebook'
import Instagram from '~/components/graphic/Instagram'
import Email from '~/components/graphic/Email'

export default {
  components: {
    PageContent,
    Logo,
    Facebook,
    Instagram,
    Email
  }
}
</script>

<style lang="scss" scoped>
.main-footer {
  height: 360px;
  padding: 60px;
  background: $lightGray;

  .content {
    display: flex;
    justify-content: space-between;

    .wrapper {
      display: flex;
      justify-content: space-between;
      flex: 1;
      width: $halfScreenCalc;

      .info {
        display: flex;
        flex-direction: column;

        .info-heading {
          color: $darkGray;
          margin-bottom: 30px;

          font-style: normal;
          font-weight: 600;
          font-size: 16px;
          line-height: 20px;
        }

        .info-link {
          color: $darkGray;
          margin-bottom: 20px;
          text-decoration: none;

          font-style: normal;
          font-weight: normal;
          font-size: 16px;
          line-height: 20px;

          &:hover {
            text-decoration: underline;
            color: $brand;
          }
        }
      }

      .contact {
        margin-left: 100px;

        .social-wrapper {
          display: flex;

          .social {
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            margin-right: 20px;
            transition: $duration opacity;

            &:hover {
              opacity: $hoverOpacity;
            }
          }
        }
      }
    }
  }
}
</style>
