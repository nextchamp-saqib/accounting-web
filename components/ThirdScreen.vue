<template>
  <div id="scrollAnimation" class="screen container d-flex">
    <img class="path" src="/Path 2.png">
    <div class="card">
      <Coa v-if="currentTimeline === 't1'" @completed="onComplete"/>
      <Setup v-if="currentTimeline === 't2'" @completed="onComplete"/>
    </div>
    <div class="card-info">
      <div class="card-title">{{ title }}</div>
      <div class="card-description">{{ description }}</div>
    </div>
  </div>
</template>

<script>
import Coa from './svgs/Coa'
import Setup from './svgs/Setup'

export default {
  name: 'ThirdScreen',
  components: {
    Coa,
    Setup
  },
  data() {
    return {
      currentTimeline: 't1'
    }
  },
  computed: {
    title() {
      return this.currentTimeline === 't1' ? 'Chart of Accounts' : 'Easy Setup'
    },
    description() {
      return this.currentTimeline === 't1'
        ? 'Country-wise chart of accounts.'
        : 'Super easy setup'
    }
  },
  methods: {
    onComplete(data) {
      this.currentTimeline = 't' + data
    }
  }
}
</script>

<style lang="sass" scoped>
.screen
  position: relative
.card
  width: 36vw
  height:  42vh
  margin: auto 5vw
  border: none
  box-shadow: 0px 0px 10px rgba(0,0,0,0.2)
  padding: 2vw

.path
  position: absolute
  bottom: 15vh
  left: -24px
  width: 48vw


.card-info
  width: 36vw
  height:  42vh
  margin: auto 5vw
  border: none
  text-align: left

.card-title
  margin: 14px auto
  font-weight: bold
  font-size: 40px
  opacity: 0

.card-description
  font-size: 20px
  opacity: 0
</style>
