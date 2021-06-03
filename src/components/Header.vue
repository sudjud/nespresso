<template>
  <div class="header">
    <div class="header__logos">
      <img src="../assets/nespresso.png" alt=""><span class="multiply">×</span>
      <img src="../assets/kinopoisk.png" alt="">
    </div>
    <div class="header__menu">
      <a 
      :href = item.ref
      v-for="item in menuList" 
      :key="item.menuList"
      :class="{'header__menu-item_active': item.class == this.active}"
      class = 'header__menu-item'
      v-on:click="makeActive(item.class)"
      >
      {{ item.item }}
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      menuList:[
        {
          item: 'Конкурс',
          class: 'competition',
          ref: '#main'
        },
        {
          item: 'Жюри',
          class: 'jury',
          ref: '#jury'
        },
        {
          item: 'Победители',
          class: 'winners',
          ref: '#winners'
        },
      ],
      active: ''
    }
  },
  methods:{
    makeActive(item){
      this.active = item
    }
  }
}
</script>

<style lang="sass">

.multiply
  color: white
  opacity: 0.5
  margin-right: 14px
  margin-left: 10px
.header
  display: flex
  justify-content: space-around
  padding-top: 45px
  padding-bottom: 35px
  align-items: center
  &__logos
    color: white
    display: flex
    align-items: center
  &__menu
    display: flex
    color: white
    text-transform: uppercase
    font-size: 22px
    line-height: 28px
    &-item
      text-decoration: none
      margin-left: 35px
      &_active
        opacity: 0.5

</style>
