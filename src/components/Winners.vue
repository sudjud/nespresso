<template>
  <div class="winners">
    <div class="winners__top">
      <div id="winners" class="winners__top-title">Победители</div>
      <div class="winners__top-sub">NESPRESSO TALENTS 2021</div>
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
  &__top
    text-align: center
    text-transform: uppercase
    &-title
      font-size: 80px
      line-height: 103%
    &-sub
      font-size: 50px
      line-height: 103%
      letter-spacing: 0.05em
      color: #8D8372
      padding-top: 10px

</style>