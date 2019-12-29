<template>
  <div class="app">
    <main-header />
    <page-content>
      <content-slide>
        <info-block slot="info">
          <template slot="heading">Прокачай своё тело и свой кошелёк</template>
          <template slot="content">
            <p>
              <brand-text>ConstaFit</brand-text> мотивирует своих пользователей
              регулярно заниматься спортом и даёт возможность на этом
              заработать.
            </p>
            <p>
              Познакомься со своим новым тренером, которому нужно платить только
              за пропущенные тренировки!
            </p>
          </template>
          <template slot="actions">
            <button-input primary>Зарегистрироваться</button-input>
            <button-input>Пробная тренировка</button-input>
          </template>
        </info-block>
      </content-slide>
      <main-svg class="main-svg" />
    </page-content>
    <separator-slide :type="1">Чтобы стать лучше</separator-slide>
    <page-content>
      <content-slide>
        <info-block slot="info">
          <template slot="heading">
            Преврати заботу о здоровье в развлечение
          </template>
          <template slot="content">
            <p>
              С <brand-text>ConstaFit</brand-text> ежедневная тренировочная
              рутина превращается в увлекательное соревнование, по окончанию
              которого можно выиграть настоящий денежный приз!
            </p>
            <p>
              Все, что для этого нужно - следовать простым шагам мотивирует
              своих пользователей регулярно заниматься спортом и даёт
              возможность на этом заработать.
            </p>
          </template>
          <template slot="actions">
            <button-input primary>Уже хочу начать!</button-input>
          </template>
        </info-block>
        <slider slot="slider" />
      </content-slide>
    </page-content>
    <separator-slide :type="2"
      >Встроить спорт в свою жизнь куда проще, чем кажется</separator-slide
    >
    <page-content>
      <content-slide reversed>
        <info-block slot="info">
          <template slot="heading">
            Ключ к успеху - постоянство
          </template>
          <template slot="content">
            <p>
              Убедись, что всего 10 минут упражнений в день достаточно, чтобы
              укрепить физическую форму, улучшить самочувствие и сделать первый
              шаг в мир спорта!
            </p>
          </template>
          <template slot="actions">
            <button-input primary>Начинаем прямо сейчас!</button-input>
          </template>
        </info-block>
        <slider slot="slider" last-three />
      </content-slide>
    </page-content>
    <page-content>
      <content-slide>
        <info-block slot="info">
          <template slot="heading">
            Мы прогрессируем вместе с тобой
          </template>
          <template slot="content">
            <p>
              В данный момент для распознавания доступны только приседания, но
              по мере развития системы будут добавляться новые упражнения, а
              также появится возможность отслеживать тренировки с помощью камеры
              телефона.
            </p>
            <p>
              В скором времени вместе с ConstaFit ты сможешь детально
              прорабатывать всё своё тело, а также заниматься по различным
              программам тренировок от профессиональных спортсменов и тренеров!
            </p>
          </template>
          <template slot="actions">
            <button-input primary>Зарегистрироваться</button-input>
            <button-input>Пробная тренировка</button-input>
          </template>
        </info-block>
      </content-slide>
      <progress-svg class="progress-svg" />
    </page-content>
    <main-footer />
  </div>
</template>

<script>
import MainHeader from '~/components/layout/MainHeader'
import MainFooter from '~/components/layout/MainFooter'
import PageContent from '~/components/layout/PageContent'

import ContentSlide from '~/components/ContentSlide'
import SeparatorSlide from '~/components/SeparatorSlide'

import BrandText from '~/components/typeface/BrandText'

import ButtonInput from '~/components/input/ButtonInput'

import InfoBlock from '~/components/InfoBlock'

import Slider from '~/components/Slider'

import MainSvg from '~/components/graphic/Main'
import ProgressSvg from '~/components/graphic/Progress'

export default {
  components: {
    MainHeader,
    MainFooter,
    PageContent,
    ContentSlide,
    SeparatorSlide,
    BrandText,
    ButtonInput,
    InfoBlock,
    Slider,
    MainSvg,
    ProgressSvg
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Montserrat:200,400,500,600,700,800&display=swap&subset=cyrillic');

.app {
  font-family: 'Montserrat', sans-serif;
  display: flex;
  flex-direction: column;
  overflow: hidden;

  .main-svg {
    position: absolute;
    right: -160px;
    top: 30px;
    z-index: -1;
  }

  .progress-svg {
    position: absolute;
    right: 0;
    top: 100px;
    z-index: -1;
  }
}
</style>
