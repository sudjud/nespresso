<template>
  <div class="header">
    <div class="header__logos">
      <img src="../assets/nespresso.png" alt=""><span class="multiply">×</span>
      <img src="../assets/kinopoisk.png" alt="">
    </div>
    <div class="header__menu">
      <a class="header__menu-item" href="#competition">Конкурс</a>
      <a class="header__menu-item" href="#jury">Жюри</a>
      <a class="header__menu-item" href="#winners">Победители</a>
    </div>
  </div>
</template>

<style lang="sass">

.multiply
  color: white
  opacity: 0.5
  margin-right: 14px
  margin-left: 10px
.header
  display: flex
  justify-content: space-around
  padding-top: 45px
  padding-bottom: 35px
  align-items: center
  &__logos
    color: white
    display: flex
    align-items: center
  &__menu
    display: flex
    color: white
    text-transform: uppercase
    font-size: 22px
    line-height: 28px
    &-item
      text-decoration: none
      margin-left: 35px

</style>
