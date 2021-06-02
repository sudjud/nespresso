<template>
  <div class="main">
    <div class="main__top">
      <div class="main__top-title">
        NESPRESSO
      </div>
      <div class="main__top-small">
        TALENTS 2021
      </div>
    </div>

    <div class="main__play"><img src="../assets/filled-play.png" alt=""></div>
    <About />
    <Jury />
  </div>
</template>

<script> 
import About from './About'
import Jury from './Jury'
export default {
  components:{
    About,
    Jury
  }
}
</script>

<style lang="sass">
.main
  background: url('../assets/bgc.png') center top no-repeat
  -webkit-box-shadow: 0px 0px 68px 100px rgba(29, 26, 24, 1) inset
  -moz-box-shadow: 0px 0px 68px 100px rgba(29, 26, 24, 1) inset
  box-shadow: 0px 0px 68px 100px rgba(29, 26, 24, 1) inset
  padding-top: 65px
  width: 1209px
  margin: auto
  &__top
    text-align: center
    &-title
      font-size: 120px
      font-weight: 700
    &-small
      font-size: 80px
      font-weight: 400
      margin-top: 10px
  &__play
    text-align: center
    margin-top: 26px
</style>
