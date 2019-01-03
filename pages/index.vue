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
import Footer from '~/components/Footer'

export default {
  components: {
    LandingScreen,
    FeaturesScreen,
    TransitionScreen,
    Footer
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
.main-footer {
  min-width: 100vw;
  background-color: rgba(0, 0, 0, 0.7);
}
</style>
