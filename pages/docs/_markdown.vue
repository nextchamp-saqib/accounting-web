<template>
  <div class="container">
    <div id="docs-view" class="container d-flex align-items-center" v-html="markdown"/>
  </div>
</template>

<script>
import hello from './hello.md'

export default {
  computed: {
    markdown() {
      return hello
    }
  }
}
</script>

<style scoped>
.container {
  min-height: 100vh;
  font-size: 2rem;
}
#docs-view {
  position: relative;
  top: 5em;
}
</style>
