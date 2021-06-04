<template>
  <div class="carousel2">
    <div
        :class="{ carousel2__btn_hidden : positionSlider > songData.length - 3 }"
        ref="next"
        @click="next"
        class="carousel2__btn carousel2__btn-next"
      >
        <img src="../assets/next.png" alt="">
      </div>
    <div 
    class="carousel2__wrapper"
    :style="{ transform : 'translateX(' + move + 'px)' }"
    >
      <Card
        v-for="(item, index) in songData"
        :key="item.song"
        :data="item"
        @click="switchActive(index)"
        :class="{ carousel2__card_active: index === positionSlider }"
        class="carousel2__card"
        :style="{ opacity: 1 - (Math.max( Math.abs(index - positionSlider) * .1, 0)) }"
      />
    </div>
      
      <div
        :class="{ carousel2__btn_hidden : positionSlider < 2 }"
        ref="prev"
        @click="prev"
        class="carousel2__btn carousel2__btn-prev"
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
  el: "#carousel2",
  methods: {
    next() {
      if (this.positionSlider === this.songData.length) {
        return;
      }
      this.positionSlider++;
    },
    prev() {
      if (this.positionSlider === -1) {
        return;
      }
      this.positionSlider--;
    },
    switchActive(index){
      this.positionSlider = index
    }
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
        {
          song: "Тапочки Цинелас",
          singer: "Чарлин Тупас",
          background: toopasImg,
        },
        {
          song: "Тапочки Цинелас",
          singer: "Чарлин Тупас",
          background: toopasImg,
        },
        {
          song: "Тапочки Цинелас",
          singer: "Чарлин Тупас",
          background: toopasImg,
        },
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
    }
  }
};
</script>

<style lang="sass">
.carousel2
  padding-top: 130px
  display: flex
  justify-content: center
  overflow: hidden
  background: rgb(224,223,217)
  background: linear-gradient(0deg, rgba(234,231,225,1) 0%, rgba(239,234,228,1) 100%)
  &__card
    position: relative
    transition: all .7s
    transform: scale(0.98)
    margin-right: 10px
    margin-left: 10px
    &:hover
      transform: scale(1)
    @media screen and (max-width: 1200px)
      margin-left: 0 
      margin-right: 0px
    img
      display: block
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
    flex-shrink: 0
    justify-content: center
    align-items: center
    font-size: 26px
    cursor: default
    position: relative
    &_hidden
      visibility: hidden
    @media screen and (max-width: 1200px)
      display: none
    img
      height: 20px
    &-next
      top: 330px
      left: 2100px
      z-index: 100
      @media screen and (max-width: 1200px)
        top: 190px
        left: 470px
      &:hover
        transform: scale(1.1)
      &:active
        transform: scale(0.9)
    &-prev
      top: 330px
      right: 2100px
      @media screen and (max-width: 1200px)
        top: 190px
        right: 470px
      &:hover
        transform: scale(1.1)
      &:active
        transform: scale(0.9)

</style>