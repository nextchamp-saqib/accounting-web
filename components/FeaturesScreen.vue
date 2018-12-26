<template>
  <div class="screen container d-flex">
    <div class="card">
      <div class="card-image"/>
      <div class="card-title">Feature Name</div>
      <div
        class="card-description"
      >Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.</div>
    </div>
    <div class="card">
      <div class="card-image"/>
      <div class="card-title">Feature Name</div>
      <div
        class="card-description"
      >Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.</div>
    </div>
    <div class="card">
      <div class="card-image"/>
      <div class="card-title">Feature Name</div>
      <div
        class="card-description"
      >Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FeaturesScreen'
}
</script>

<style lang="sass" scoped>
.card
  background-color: rgba(255,255,255,0)
  width: 240px
  margin: auto 5vw
  border: none
.card-image
  background-color: rgba(250,250,250,1)
  border: none
  border-radius: 0
  box-shadow: 0px 0px 10px rgba(0,0,0,0.2)
  width: 100%
  height: 240px
.card-title
  margin: 14px auto
  font-weight: bold
  font-size: 28px
.card-description
  font-size: 16px
</style>
