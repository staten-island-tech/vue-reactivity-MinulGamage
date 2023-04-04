<script>
import { monkeys } from '../array'
import CartBox from '../components/cartTemplate.vue'
import boxTemplate from '../components/boxTemplate.vue'

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
      :buttonLabel="`Remove From Cart`"
    />
  </div>
</template>

<style>
.CartBox {
  border: 4px solid black;
  border-radius: 10%;
  width: 30vw;
  height: 90vh;
  margin: 40px auto;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
}

.box:hover {
  transform: scale(105%);
}

.name {
  text-align: center;
  font-size: 3rem;
  font-weight: bold;
}
.image {
  width: 25vw;
  height: 40vh;
  justify-content: center;
  margin: 10px auto;
  text-align: center;
  border: 3px solid black;
  border-radius: 5%;
}
.price {
  text-align: center;
}

.Buy {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  width: 10vw;
}
.Habitat {
  text-align: center;
}
.dangerous {
  text-align: center;
}
body {
  background-color: cadetblue;
}
</style>
