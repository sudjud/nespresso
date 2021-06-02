<template>
  <div class="winners">
    <div class="winners-top">
      <div class="winners-top__title">Победители</div>
      <div class="winners-top__sub">NESPRESSO TALENTS 2021</div>
    </div>
    <Carousel />
  </div>
</template>

<script>
import Carousel from './Carousel'
export default {
  components:{
    Carousel
  },
};
</script>

<style lang="sass">
.winners
  padding-top: 267px
.winners-top
  text-align: center
  text-transform: uppercase
  &__title
    font-size: 80px
    line-height: 103%
  &__sub
    font-size: 50px
    line-height: 103%
    letter-spacing: 0.05em
    color: #8D8372
    padding-top: 10px

</style>