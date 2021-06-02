<template>
  <div class="finalists">
    <div class="winners-top finalists-top">
      <div class="winners-top__title">Финалисты</div>
      <div class="winners-top__sub">NESPRESSO TALENTS 2021</div>
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
</style>