<template>
  <div
    ref="some"
    class="card"
    id="card"
    :style="{ backgroundImage: `url(${data.background}` }"
  >
    <div class="card__top">
      <div class="card__top-song"> {{ data.song }}</div>
      <div class="card__top-singer">{{ data.singer }} </div>
    </div>
    <img src="../assets/play.png" alt="" />
    <div class="card__footer">
      <div class="card__footer-place">
        <div class="card__footer-place-number">1</div>
        <div>место</div>
      </div>
      <div>Россия</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Object,
  }
}
</script>

<style lang="sass">
.card
  text-align: center
  width: 393px
  height: 700px
  display: flex
  flex-direction: column
  justify-content: space-between
  background-clip: padding-box
  background-size: 100%
  transform: scale(0.8)
  opacity: 0.3
  transition: transform .5s
  transition: opacity .5s
  @media screen and (max-width: 1200px)
    height: 400px
    width: 224px
  &_active
    transform: scale(1)
    opacity: 1
  img
    margin: 0 auto
    display: none
    &:hover
      transform: scale(1.1)
    @media screen and (max-width: 1200px)
      transform: scale(0.56)
  &__top
    text-align: center
    padding: 50px 
    text-transform: none
    @media screen and (max-width: 1200px)
      padding: 28px
    &-song
      font-size: 30px
      line-height: 30px
      color: #FFFFFF
      padding-bottom: 10px
      @media screen and (max-width: 1200px)
        font-size: 17px
        line-height: 17px
    &-singer
      font-size: 20px
      line-height: 24px
      color: #F1EDE7
      opacity: 0.7
      @media screen and (max-width: 1200px)
        font-size: 11px
        line-height: 13px
  &__footer
      display: flex
      justify-content: space-between
      align-items: flex-end
      font-size: 18px
      text-transform: uppercase
      padding: 0 25px 25px 25px
      color: #8D8372
      @media screen and (max-width: 1200px)
        font-size: 10px
      &-place-number
        font-size: 100px
        line-height: 100px
        @media screen and (max-width: 1200px)
          font-size: 56px
          line-height: 56px
</style>