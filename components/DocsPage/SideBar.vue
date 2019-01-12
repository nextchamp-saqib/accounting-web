<template>
  <div class="container">
    <nuxt-link :to="'/docs/quick-start'">Quick Start</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/setting-up'">Setting Up</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/chart-of-accounts'">Chart of Accounts</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/item'">Item</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/party'">Party</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/tax'">Tax</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/invoice'">Invoice</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/payment'">Payment</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/general-ledger'">General Ledger</nuxt-link>
    <br>
    <nuxt-link :to="'/docs/sales-register'">Sales Register</nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'SideBar'
}
</script>


<style lang="sass" scoped>
a 
  color: #455a64
  &:hover
    color: black
    text-decoration: none

.container
  position: relative;
  top: 3em;
  left: 5em;
  min-height: 100vh;
  font-size: 1rem;

</style>
