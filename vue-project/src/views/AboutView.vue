<script>
import { monkeys } from '../array'
import CartBox from '../components/icons/cartTemplate.vue'

export default {
  name: 'ShoppingCart',
  components: { CartBox },
  data() {
    return {
      monkeys,
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
    <CartBox
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
