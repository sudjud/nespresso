<template>
  <div class="about">
    <div class="about__hashs">
      #NESPRESSOTALENTS<br />
      #DOINGISEVERYTHING<br />
      #ДЕЛОИМЕТТЗНАЧЕНИЕ<br />
    </div>
    <div class="about__text">
      Мы в Nespresso верим, что любое дело имеет значение. И самый
      незначительный, на первый взгляд, поступок может стать ключевым для общего
      дела сохранения природы. Это убеждение стало основной темой конкурса
      Nespresso Talents 2021. Молодые режиссеры и любители кинематографа
      поделились своим видением идеи «ДЕЛО ИМЕЕТ ЗНАЧЕНИЕ», вдохновляя людей
      сохранять красоту и многообразие природы.
    </div>
  </div>
</template>

<style lang="sass">

// .about
//   display: flex
//   justify-content: space-between
//   padding-top: 114px
//   &__text
//     width: 500px
//     font-size: 22px
//     line-height: 28px
//   &__hashs
//     font-size: 30px
//     line-height: 40px

.about
  display: flex
  justify-content: space-between
  padding-top: 114px
  @media screen and (max-width: 992px)
    flex-direction: column
    padding-left: 20px
  &__text
    width: 500px
    font-size: 22px
    line-height: 28px
    @media screen and (max-width: 992px)
      margin-left: auto
      margin-top: 30px
      margin-right: 20px 
  &__hashs
    font-size: 30px
    line-height: 40px
    @media screen and (max-width: 992px)
      margin-right: auto



</style>