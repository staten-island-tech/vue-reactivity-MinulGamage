<script>
import { monkeys } from '../array'
import boxTemplate from '../components/boxTemplate.vue'

export default {
  name: 'ShoppingCart',
  components: { boxTemplate },
  data() {
    return {
      cartItems,
      currentPrice: 0,
      price: new Intl.NumberFormat('en-US', {
        style: 'currency',
        currency: 'USD'
      })
    }
  },
  methods: {}
}
</script>

<template>
  <div class="shoppingCart">
    <h1>Shopping Cart</h1>
  </div>
  <div class="Cart-Box">
    <boxTemplate
      v-for="monkey in monkeys"
      v-bind:key="monkey"
      :species="monkey.species"
      :img="monkey.img"
      :price="monkey.price"
      :Habitat="monkey.Habitat"
      :dangerous="monkey.dangerous"
      :InStock="monkey.InStock"
      :buttonLabel="`Remove From Cart`"
    />
  </div>
</template>

<style></style>
