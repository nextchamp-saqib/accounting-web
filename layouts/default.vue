<template>
  <div>
    <NavBar/>
    <nuxt/>
    <Footer/>
  </div>
</template>

<script>
import NavBar from '~/components/NavBar'
import Footer from '~/components/Footer'

export default {
  components: {
    NavBar,
    Footer
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Fira+Sans');

body {
  font-family: 'Fira Sans', sans-serif !important;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
