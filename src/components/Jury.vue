<template>
    <div class="jury">
      <div class="jury__top">
        <div class="jury__top-title">
          Работы <br>оценивали
        </div>
        <div class="about__text">
          Станьте свидетелем зарождения новых звезд кинематографа и обладателей престижных премий!
        </div>
      </div>
      <JuryInfo />
    </div>
</template>

<script>
import JuryInfo from './JuryInfo'
export default {
  components:{
    JuryInfo
  }
}
</script>

<style lang="sass">

.jury
  padding-top: 40px
  &__top
    display: flex
    justify-content: space-between
    &-title
      text-transform: uppercase
      font-size: 50px
      line-height: 51px
      font-weight: 700
      
</style>