<template>
  <div
    ref="some"
    class="card"
    id="card"
    :style="{ backgroundImage: `url(${data.background}` }"
    :class="{ 'card_active' : classItem === 0 }"
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
  margin-left: -70px
  &_active
    transform: scale(1)
    opacity: 1
  img
    margin: 0 auto
  &__top
    text-align: center
    padding: 50px 
    text-transform: none
    &-song
      font-size: 30px
      line-height: 30px
      color: #FFFFFF
      padding-bottom: 10px
    &-singer
      font-size: 20px
      line-height: 24px
      color: #F1EDE7
      opacity: 0.7
  &__footer
      display: flex
      justify-content: space-between
      align-items: flex-end
      font-size: 18px
      text-transform: uppercase
      padding: 0 25px 25px 25px
      color: #8D8372
      &-place-number
        font-size: 100px
        line-height: 100px
</style>