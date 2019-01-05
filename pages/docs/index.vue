<template>
  <div class="container">
    <div class="container row">
      <div id="sidebar" class="col-md-3">
        <SideBar/>
      </div>
      <div class="col-md-9">
        <div id="docs-view" class="container d-flex align-items-center" v-html="markdown"/>
      </div>
    </div>
  </div>
</template>

<script>
import hello from './hello.md'
import hello2 from './hello2.md'
import SideBar from '~/components/DocsPage/SideBar'

export default {
  name: 'Docs',
  components: {
    SideBar
  },
  computed: {
    markdown() {
      return hello
    }
  },
  created() {
    console.log(this.hello)
  }
}
</script>

<style lang="sass" scoped>
.container 
  min-height: 100vh;

#sidebar
  box-shadow: 2px 0px 0px 0px #eceff1

#docs-view
  position: relative;
  top: 5em
</style>
