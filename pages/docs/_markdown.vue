<template>
  <div class="container">
    <div id="docs-view" class="container d-flex align-items-center" v-html="markdown"/>
  </div>
</template>

<script>
export default {
  computed: {
    markdown() {
      var currentPath = this.$route.path.split('/')
      var renderedFile = require('./' + currentPath[2] + '.md')
      return renderedFile
    }
  }
}
</script>

<style scoped>
.container {
  min-height: 100vh;
  font-size: 1rem;
}
#docs-view {
  position: relative;
  top: 2em;
}
</style>
