<template>
  <div class="container row">
    <div class="title col-md-12">Why Frappe Accounting?</div>
    <div class="screen col-md-12 row d-flex">
      <div v-for="(feature, index) in features" :key="index" class="feature col-md-5">
        <div class="feature-title">{{ feature.title }}</div>
        <div class="feayure-description">{{ feature.desc }}}</div>
        <div class="feature-icon d-flex align-items-center">
          <img :src="feature.icon">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FeaturesScreen',
  data() {
    return {
      features: [
        {
          title: 'Free',
          desc:
            'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.',
          icon: 'free.svg'
        },
        {
          title: 'GST Ready',
          desc:
            'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.',
          icon: 'gstready.svg'
        },
        {
          title: 'Easy to use',
          desc:
            'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.',
          icon: 'easy.svg'
        },
        {
          title: 'Multicurrency',
          desc:
            'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.',
          icon: 'multicurrency.svg'
        }
      ]
    }
  }
}
</script>

<style lang="sass" scoped>
.container
  display: flex
  flex-direction: row
  justify-content: flex-start
  flex-wrap: wrap

.screen
  min-width: 90vw
  flex-wrap: wrap

.icon
  min-width: 5vw

.title
  font-size: 3rem

.feature
  background-color: rgba(249,249,249,1)
  margin: 1vw auto
  padding: 18px
  border-radius: 5px
  box-shadow: 0px 0px 15px rgba(0,0,0,0.1)
  transition: all .2s ease-in-out
  &:hover
    transform: scale(1.01)
    color: #007BFF

.feature-icon
  width: 42px
  height: 42px
  margin: 12px auto
  img
    width: 100%

.feature-title
  margin: 14px auto
  font-weight: bold
  font-size: 1.5rem

.feature-description
  font-size: 15px
</style>
