<template>
  <section>
    <div class="container">
      <LandingScreen/>
    </div>
    <div class="container">
      <FeaturesScreen/>
    </div>
    <div class="container">
      <ThirdScreen/>
    </div>
  </section>
</template>

<script>
import LandingScreen from '~/components/LandingScreen'
import FeaturesScreen from '~/components/FeaturesScreen'
import ThirdScreen from '~/components/ThirdScreen'

export default {
  components: {
    LandingScreen,
    FeaturesScreen,
    ThirdScreen
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
