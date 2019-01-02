<template>
  <div class="screen container d-flex">
    <div v-for="(feature, index) in features" :key="index" class="card">
      <div class="card-title">{{ feature.title }}</div>
      <div class="card-description">{{ feature.desc }}}</div>
      <div class="card-image"/>
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
            'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.'
        },
        {
          title: 'GST Ready',
          desc:
            'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.'
        },
        {
          title: 'Easy to use',
          desc:
            'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.'
        }
      ]
    }
  }
}
</script>

<style lang="sass" scoped>
.card
  background-color: rgba(255,255,255,1)
  // width: 240px
  margin: auto 42px
  padding: 18px
  border: 1px solid rgba(0,0,0,0.2)
  border-radius: 2%
  box-shadow: 0px 0px 15px rgba(0,0,0,0.1)

.card-image
  background-color: rgba(240,240,240,1)
  border: none
  border-radius: 100%
  box-shadow: 0px 0px 6px rgba(0,0,0,0.3)
  width: 32px
  height: 32px
  margin: 12px auto

.card-title
  margin: 14px auto
  font-weight: bold
  font-size: 28px
  color: #343A40

.card-description
  font-size: 15px
</style>
