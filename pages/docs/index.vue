<template>
  <div class="container">
    <div class="container row">
      <div class="col-md-4">
        <SideBar/>
      </div>
      <div class="col-md-8">
        <div class="container d-flex align-items-center">Docs`</div>
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
  min-height: 100vh
</style>
