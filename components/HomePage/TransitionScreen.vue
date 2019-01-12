<template>
  <div id="scrollAnimation" class="screen container d-flex">
    <div class="animation-list">
      <div class="main-title">Key Features</div>
      <div
        v-for="(item, index) in animations"
        :key="index"
        :class="setActiveClass(index)"
        class="list-item"
      >
        <div class="title">{{ item.title }}</div>
        <div v-if="index === currTranstition" class="description">{{ item.description }}</div>
      </div>
    </div>
    <div class="animation-box d-flex align-items-center">
      <img class="path" src="/transitionBackground.png">
      <div v-if="currTranstition === 0" class="animation">
        <ReportGen @completed="onComplete"/>
      </div>
      <div v-if="currTranstition === 1" class="animation">
        <Invoices @completed="onComplete"/>
      </div>
      <div v-if="currTranstition === 2" class="animation">
        <BankReconcilation @completed="onComplete"/>
      </div>
      <div v-if="currTranstition === 3" class="animation">
        <GSTR @completed="onComplete"/>
      </div>
    </div>
  </div>
</template>

<script>
import ReportGen from '../animated/ReportGen'
import GSTR from '../animated/GSTR'
import Invoices from '../animated/Invoices'
import BankReconcilation from '../animated/BankReconcilation'

export default {
  name: 'TransitionScreen',
  components: {
    ReportGen,
    Invoices,
    BankReconcilation,
    GSTR
  },
  data() {
    return {
      currTranstition: 0,
      animations: [
        {
          title: 'Automated Report Generation',
          description:
            'View all kinds of business reports and export them on the go.'
        },
        {
          title: 'Customizable Invoice templates',
          description:
            'Choose from a variety of invoice templates and customize it to best suit your business'
        },
        {
          title: 'Bank Reconciliation',
          description:
            'No more bounced cheques or overdraft fees. Reconcile your accounts to keep in sync with banking accounts.'
        },
        {
          title: 'GST Compliance',
          description: 'Automate GSTR-1 and GSTR-3B report generation.'
        }
      ]
    }
  },
  mounted() {},
  methods: {
    onComplete(data) {
      this.activeAnimation = data - 1
      this.currTranstition = data - 1
    },
    setActiveClass(index) {
      if (this.activeAnimation === index) return 'active'
      else return false
    }
  }
}
</script>

<style lang="sass" scoped>
.animation-box
  position: relative
  background: none
  width: 68vw
  height: 50vh
  // margin: auto 1vw
  border: none
  // box-shadow: 0px 0px 10px rgba(0,0,0,0.2)

  
.animation
  z-index: 1
  margin: auto auto
  position: relative
  width: 100%
  height: 100%

.path
  position: absolute
  bottom: 0vh
  left: 4vw
  width: 48vw


.animation-list
  // box-shadow: 0px 0px 10px rgba(0,0,0,0.2)
  // margin: auto 1vw
  border: none
  text-align: left

.list-item
  background-color: rgba(245,245,245,0.9)
  border-radius: 10px
  box-shadow: 0px 2px 8px rgba(0,0,0,0.1)
  padding: 14px
  width: 30vw
  font-size: 22px
  margin: 24px auto
  text-align: center
  color: #111
  transition: all 0.2s ease-in


.active
  // background-color: rgba(40,45,45,0.8)
  transition: all 0.2s ease-in
  .title
    font-weight: bold
    // text-shadow: 0px 0px 10px #007BFF
    color: #007BFF !important
  .description
    // color: rgba(255,255,255,0.9) !important

.main-title
  font-weight: bold
  font-size: 42px
  padding: 10px
  width: 30vw
  margin: 24px auto
  text-align: center
  // color: #111
  color: #007BFF

.description
  font-size: 15px

svg 
  position: absolute
  left: 0
  right: 0
  width: 100%
  height: 100%
</style>
