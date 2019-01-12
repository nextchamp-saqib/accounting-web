<template>
  <section>
    <div class="container">
      <LandingScreen/>
    </div>
    <div class="container">
      <FeaturesScreen/>
    </div>
    <div class="container">
      <TransitionScreen/>
    </div>
  </section>
</template>

<script>
import LandingScreen from '~/components/HomePage/LandingScreen'
import FeaturesScreen from '~/components/HomePage/FeaturesScreen'
import TransitionScreen from '~/components/HomePage/TransitionScreen'

export default {
  components: {
    LandingScreen,
    FeaturesScreen,
    TransitionScreen
  }
}
</script>

<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
