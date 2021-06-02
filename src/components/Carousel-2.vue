<template>
  <div class="carousel2">
    <div class="carousel2__wrapper">
      <Card 
        v-for="item in songData"
        :key="item.song"
        :data="item"
        class="carousel2__item"
      />
    </div>
  </div>
</template>

<script>
import Card from "./Card";
import petrovImg from "../assets/mpetrov.png";
import toopasImg from "../assets/toopas.png";
import someelseImg from "../assets/someelse.png";
import fourthImg from "../assets/son-and-mother.png"
export default {
  components:{
    Card
  },
  data() {
    return {
      positionSlider: 0,
      songData: [
        {
          song: "Кофейное счастье",
          singer: "Михаил Петров",
          background: petrovImg,
        }
      ],
    };
  },
};
</script>

<style lang="sass">

.carousel2
  padding-top: 84px
  display: flex
  justify-content: center
  &__wrapper
    display: flex
  &__item
    opacity: 1
    transform: scale(1)
    margin-right: 23px

</style>