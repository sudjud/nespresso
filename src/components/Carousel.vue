<template>
  <div id="carousel" class="carousel">
    <div class="carousel__wrapper">
      <Card
        id="card"
        v-for="(item, index) in songData"
        :key="item.song"
        :data="item"
        :class="{ carousel__card_active: index === positionSlider }"
        class="carousel__card"
      />
    </div>
      <div
        v-if="positionSlider !== 2"
        ref="next"
        @click="next"
        class="carousel__btn carousel__btn-next"
        id="next"
      >
        ❯
      </div>
      <div
        v-if="positionSlider !== 0"
        ref="prev"
        @click="prev"
        class="carousel__btn carousel__btn-prev"
        id="prev"
      >
        ❮
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
      if (this.positionSlider === 2) {
        return;
      }
      this.positionSlider++;
    },
    prev() {
      if (this.positionSlider === 0) {
        return;
      }
      this.positionSlider--;
    },
  },
  el: "#card",
  data() {
    return {
      positionSlider: 1,
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
};
</script>

<style lang="sass">
.carousel
  padding-top: 130px
  display: flex
  justify-content: center
  position: relative
  padding-left: 100px
  background: url('../assets/projector.png') center no-repeat
  -webkit-box-shadow: 0px 71px 96px 51px rgba(29, 26, 24, 0.97) inset
  -moz-box-shadow: 0px 71px 96px 51px rgba(29, 26, 24, 0.97) inset
  box-shadow: 0px 71px 96px 51px rgba(29, 26, 24, 0.97) inset
  padding-bottom: 106px
  &__card_active
    transform: scale(1)
    opacity: 1
    z-index: 5
  &__card
    margin-left: -70px
  &__wrapper
    display: flex
    position: relative
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
    padding-right: 3px
    cursor: default
    position: relative
    &-next
      top: 330px
      right: 220px
      &:hover
        transform: scale(1.1)
      &:active
        transform: scale(0.9)
    &-prev
      top: 330px
      right: 930px
      &:hover
        transform: scale(1.1)
      &:active
        transform: scale(0.9)
</style>