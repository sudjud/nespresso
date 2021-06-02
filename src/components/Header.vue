<template>
  <div class="header">
    <div class="logos">
      <img src="../assets/nespresso.png" alt=""><span class="multiply">×</span>
      <img src="../assets/kinopoisk.png" alt="">
    </div>
    <div class="menu">
      <a class="menu__item" href="#competition">Конкурс</a>
      <a class="menu__item" href="#jury">Жюри</a>
      <a class="menu__item" href="#winners">Победители</a>
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
.logos
  color: white
  display: flex
  align-items: center
.menu
  display: flex
  color: white
  text-transform: uppercase
  font-size: 22px
  line-height: 28px
  &__item
    text-decoration: none
    margin-left: 35px

</style>
