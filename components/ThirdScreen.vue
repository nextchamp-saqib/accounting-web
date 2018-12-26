<template>
  <div id="scrollAnimation" class="screen container d-flex">
    <img class="path" src="/Path 2.png">
    <div class="card">
      <coa/>
    </div>
    <div class="card-info">
      <div class="card-title">Chart of Accounts</div>
      <div class="card-description">Country-wise chart of accounts.</div>
    </div>
  </div>
</template>

<script>
import Coa from './svgs/Coa'

export default {
  name: 'ThirdScreen',
  components: {
    Coa
  },
  beforeMount() {}
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
