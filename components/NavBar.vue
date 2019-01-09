<template>
  <div class="navbar">
    <div class="navbar-left">
      <img class="frappe-logo" src="/logo.png">
      <nuxt-link to="/">
        <div class="company-name">Frappe</div>
      </nuxt-link>
    </div>
    <div class="navbar-right">
      <nuxt-link to="/docs">Docs</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {}
  }
}
</script>

<style lang="sass" scoped>
a
  color: #455a64
  &:hover
    color: black
    text-decoration: none

.navbar
  position: fixed
  width: 100%
  background-color: rgba(255,255,255,1)
  z-index: 3
  display: flex
  box-shadow: 0px 1px 6px rgba(0,0,0, 0.1)
  padding: 5px 12rem
  .navbar-right
    margin: 10px 0
    margin-left: auto
    a
      margin: 10px 16px
      font-size: 18px

  .navbar-left
    display: flex
    margin: 0 70px;
    .company-name
      margin: 0 5px
      font-size: 20px
      font-weight: bold
    .frappe-logo
      width: 32px
      height: 32px

</style>
