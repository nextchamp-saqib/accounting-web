<template>
  <div class="container d-flex">
    <img src="background.png">
    <div class="title">
      <h1 class="bold">Frappe Accounting</h1>
      <p>Offline Accounting software for everyone,
        <br>with Invoicing, Payments and Reports.
      </p>
      <button class="btn btn-default">Download Now!</button>
    </div>
    <div class="svgIcon">
      <Logo/>
    </div>
  </div>
</template>

<script>
import Logo from '../animated/Logo'

export default {
  name: 'LandingScreen',
  components: {
    Logo
  }
}
</script>

<style lang="sass" scoped>
.container
  position: relative

img
  position: absolute
  top: 60px
  width: 100vw
  height: 190vh
  z-index: 0

.title
  z-index: 1
  margin: auto 5vw auto 0vw
  text-align: left
  font-size: 17px
  h1
    font-size: 42px
    font-weight: bold
  .btn-default
    color: white
    background-color: rgba(0,0,0,0.8)
    box-shadow: 0px 0px 15px rgba(0,0,0,0.1)

.svgIcon
  z-index: 1
  margin: auto 0vw auto 5vw

</style>
