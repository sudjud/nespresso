<template>
  <div >
    <Header />
    <Main />
    <Winners />
    <Finalists />
  </div>
</template>

<script>
import Header from './components/Header'
import Main from './components/Main'
import Winners from './components/Winners'
import Finalists from './components/Finalists'
// import Card from './components/Card'

export default {

  components: {
    Header,
    Main,
    Winners,
    Finalists
    // Card
  }
}
</script>

<style lang="sass">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap');
body, html
  margin: 0
#app
  margin: auto
  background-color: #1D1A18
  font-family: 'Montserrat', sans-serif
  color: #F1EDE7
a
  color: white
  text-decoration: none

</style>
