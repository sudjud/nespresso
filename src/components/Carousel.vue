<template>
  <div class="carousel">
    <div
        :class="{ carousel__btn_hidden : positionSlider == songData.length - 1 }"
        ref="next"
        @click="next"
        class="carousel__btn carousel__btn-next"
      >
        <img src="../assets/next.png" alt="">
      </div>
    <div 
    class="carousel__wrapper"
    :style="{ transform : 'translateX(' + move + 'px)' }"
    >
      <Card
        v-for="(item, index) in songData"
        :key="item.song"
        :data="item"
        :class="{ carousel__card_active: index === positionSlider }"
        :style="{ transform: 'scale('+ (1 - (Math.max( Math.abs(index - positionSlider) * .1, 0))) +')', opacity: 1 - (Math.max( Math.abs(index - positionSlider) * .4, 0)) }"
        class="carousel__card"
      />
    </div>
      
      <div
        :class="{ carousel__btn_hidden : positionSlider == 0 }"
        ref="prev"
        @click="prev"
        class="carousel__btn carousel__btn-prev"
      >
        <img src="../assets/prev.png" alt="">
      </div>
  </div>
</template>

<script>
import Card from "./Card";
import petrovImg from "../assets/mpetrov.png";
import toopasImg from "../assets/toopas.png";
import someelseImg from "../assets/someelse.png";
export default {
  el: "#carousel",
  methods: {
    next() {
      if (this.positionSlider === this.songData.length) {
        return;
      }
      this.positionSlider++;
      
      console.log(this.scale);
    },
    prev() {
      if (this.positionSlider === -1) {
        return;
      }
      this.positionSlider--;
      console.log(this.scale);
    },
  },
  el: "#card",
  data() {
    return {
      positionSlider: 1,
      step: 300,
      songData: [
        {
          song: "Кофейное счастье",
          singer: "Михаил Петров",
          background: petrovImg,
        },
        {
          song: "Тапочки Цинелас",
          singer: "Чарлин Тупас",
          background: toopasImg,
        },
        { song: "Третья песня", singer: "Третье имя", background: someelseImg },
      ],
    };
  },
  components: {
    Card,
  },
  computed:{
    move(){
      const windowWidth = window.innerWidth
      const x = windowWidth > 1200 ? 1 : 1.7
      return (((Math.round((this.songData.length - 1)) / 2) - this.positionSlider) * this.step) / x;
    },
    scale(prop){
      return 1 - Math.abs((Math.round(this.songData.length / 2 - 1) - this.positionSlider) / 10)
    }
  }
};
</script>

<style lang="sass">
.carousel
  padding-top: 130px
  display: flex
  justify-content: center
  background: url('../assets/projector.png') center no-repeat
  -webkit-box-shadow: 0px 71px 96px 51px rgba(29, 26, 24, 0.97) inset
  -moz-box-shadow: 0px 71px 96px 51px rgba(29, 26, 24, 0.97) inset
  box-shadow: 0px 71px 96px 51px rgba(29, 26, 24, 0.97) inset
  padding-bottom: 106px
  overflow: hidden
  &__card
    margin-left: -35px 
    margin-right: -35px
    position: relative
    transition: all .7s
    @media screen and (max-width: 1200px)
      margin-left: -20px 
      margin-right: -20px
    &_active
      transform: scale(1)
      opacity: 1
      z-index: 5
      img
        display: block
    &_small_left
      transform: scale(0.4) translateX(-300px)
      opacity: 0.1
      position: relative
      z-index: 0
    &_small_right
      transform: scale(0.4) translateX(300px)
      opacity: 0.1
      position: relative
      z-index: 0
  &__wrapper
    display: flex
    position: relative
    transition: all .5s
  &__btn
    height: 56px
    width: 56px
    border-radius: 50%
    background-color: white
    color: black
    display: flex
    justify-content: center
    align-items: center
    font-size: 26px
    cursor: default
    position: relative
    z-index: 100
    &_hidden
      visibility: hidden
    @media screen and (max-width: 1200px)
      width: 20px 
      height: 20px
      img
        height: 10px
    &-next
      top: 330px
      left: 830px
      @media screen and (max-width: 1200px)
        top: 190px
        left: 470px
      &:hover
        transform: scale(1.1)
      &:active
        transform: scale(0.9)
    &-prev
      top: 330px
      right: 830px
      @media screen and (max-width: 1200px)
        top: 190px
        right: 470px
      &:hover
        transform: scale(1.1)
      &:active
        transform: scale(0.9)

</style>