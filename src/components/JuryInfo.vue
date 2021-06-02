<template>
  <div class="jury-info">
    <div class="jury-info__perisild-photo">
      <img src="../assets/perisild.png" alt="" />
    </div>

    <div class="jury-info__all">
      <div class="jury-info__perisild">
        <div class="jury-info__perisild-name">Юлия Перисильд</div>
        <div class="jury-info__perisild-label">
          <div class="jury-info__label-wrap">
            Председатель жюри Nespresso Talents 2021
          </div>
        </div>
      </div>
      <div class="jury-info__job">Актриса театра и кино</div>

      <div class="jury-info_line"></div>
      <div class="jury-others">
        <div class="jury-others__item">
          Ирина Понарушку<br />
          <span class="jury-info__job">Актер театра и кино</span>
        </div>
        <div class="jury-others__item">
          Нателла Крапивина<br />
          <span class="jury-info__job">Актер театра и кино</span>
        </div>
        <div class="jury-others__item">
          Ирина Ситдикова<br />
          <span class="jury-info__job">Актер театра и кино</span>
        </div>
        <div class="jury-others__item">
          Александр Молочников<br />
          <span class="jury-info__job">Актер театра и кино</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import JuryOthers from "./JuryOthers";
export default {
  components: {
    JuryOthers,
  },
};
</script>

<style lang="sass">
.jury-info
  padding-top: 60px
  display: flex
  padding-right: 150px
  &_line
    width: 100%
    height: 1px
    background-color: #FFFFFF
    opacity: 0.1
    margin-top: 40px
    margin-bottom: 40px
  &__all
    padding-top: 58px
    padding-left: 61px
  &__job
    font-size: 17px
    line-height: 20px
    color: #8D8372
    margin-top: 10px
  &__label-wrap
    width: 77%
    margin: auto
  &__perisild
    display: flex
    padding-bottom: 5px
    &-name
      font-size: 50px
      line-height: 45px
      padding-right: 30px
    &-label
      color: #8D8372
      border: 2px solid #8D8372
      font-size: 20px
      font-weight: 600
      display: flex
      align-items: center
.jury-others
  display: flex
  justify-content: space-between
  flex-wrap: wrap
  &__item
    font-size: 26px
    line-height: 31px
    width: 50%
    padding-bottom: 40px
</style>