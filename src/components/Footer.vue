<template>
  <div class="footer">
    <div class="footer__container">
      <div class="footer__img">
        <div class="footer__img-wrapper"><img src="../assets/letter-N.png" alt=""></div>
        <div class="footer__img-wrapper"><img src="../assets/and.png" alt=""></div>
        <div class="footer__img-wrapper"><img src="../assets/infinity.png" alt=""></div>
      </div>
      <div class="footer__title">
        Эко-партнёр Nespresso Talents 2021 в России – Сфера Экологии, учредили специальный приз для участников конкурса.
      </div>
      <div class="footer__subtitle">
        Мы объеденяем свои усилия по восстановлению лесов и высадим деревья за каждый присланный фильм.
      </div>
      <div class="footer__subscribe">
        <div class="footer__subscribe_left">
          ПОДПИШИТЕСЬ НА NESPRESSO <span style='color: #00A536'>#NESPRESSOTALENTS</span>
        </div>
        <div class="footer__subscribe_right">
          <img class="footer__subscribe_img" src="../assets/youtube.png" alt="">
          <img class="footer__subscribe_img" src="../assets/facebook.png" alt="">
          <img class="footer__subscribe_img" src="../assets/twitter.png" alt="">
          <img class="footer__subscribe_img" src="../assets/instagram.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="sass">

@mixin container
  width: 1140px
  margin: 0 auto
  max-width: calc( 100% - 80px )

.footer
  color: #F1EDE7
  text-align: center
  background-image: linear-gradient(0deg, rgba(11,43,22,1) 10%, rgba(239,234,228,0) 71%), url('../assets/bg-forest.jpg')
  background-size: 100%
  background-position-y: 165%
  @media screen and (max-width: 1700px)
    background-position-y: 0
    background-image: linear-gradient(0deg, rgba(11,43,22,1) 25%, rgba(239,234,228,0) 50%), url('../assets/bg-forest.jpg')
  @media screen and (max-width: 1250px)
    background-position-y: 0
    background-image: linear-gradient(0deg, rgba(11,43,22,1) 35%, rgba(239,234,228,0) 71%), url('../assets/bg-forest.jpg')
  &__container
    @include container
  &__img
    margin-left: 17px
    margin-right: 17px
    display: flex
    justify-content: center
    align-items: center
    padding-top: 284px
    &-wrapper
      margin-left: 17px
      margin-right: 33px
  &__title
    font-size: 30px
    line-height: 36px
    padding-top: 63px
    font-weight: 400
  &__subtitle
    font-size: 22px
    line-height: 28px
    padding-top: 30px
    font-weight: 400
  &__subscribe
    display: flex
    justify-content: space-between
    padding-top: 100px
    padding-bottom: 23px
    &_img
      padding-left: 23px
    &-left 
      font-size: 20px
      line-height: 24px
      text-transform: uppercase
      font-weight: 600
    &-right
      margin-left: 23px



</style>