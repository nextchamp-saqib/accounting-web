<template>
  <div class="container">
    <nuxt-link :to="'/docs/hello'">User</nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'SideBar'
}
</script>


<style scoped>
.container {
  position: relative;
  top: 3em;
  left: 2em;
  min-height: 100vh;
  font-size: 2rem;
}
</style>
