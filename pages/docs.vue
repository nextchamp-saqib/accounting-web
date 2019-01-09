<template>
  <div class="container">
    <div class="container row">
      <div id="sidebar" class="col-md-3">
        <SideBar/>
      </div>
      <div class="col-md-9">
        <nuxt-child/>
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from '~/components/DocsPage/SideBar'

export default {
  name: 'Docs',
  components: {
    SideBar
  }
}
</script>

<style lang="sass" scoped>
.container
  padding-top: 4vh
  min-height: 100vh

#sidebar
  box-shadow: 2px 0px 0px 0px #eceff1
</style>
