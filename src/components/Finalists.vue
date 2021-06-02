<template>
  <div class="finalists">
    <div class="finalists__top">
      <div class="finalists__top-title">Финалисты</div>
      <div class="finalists__top-sub">NESPRESSO TALENTS 2021</div>
    </div>
    <Carousel-2 />
  </div>
</template>

<script>
import Carousel2 from './Carousel-2'
export default {
  components:{
    Carousel2
  }
}
</script>

<style lang="sass">
.finalists
  background-color: #F1EDE7
  padding-top: 130px
  color: #8D8372
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