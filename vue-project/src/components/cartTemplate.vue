<script>
import { monkeys } from './boxTemplate.vue'
export default {
  name: 'CartBox',
  data() {
    return {
      monkeys
    }
  },
  methods: {
    removefromShoppingCart(object) {
      console.log(object)
      let box = monkey.find((monkey) => monkey.species === object.species)
      monkeys.splice(box, 1)
    }
  }
}
</script>

<template>
  <div class="CartBox">
    <h2 class="Cartname">{{ species }}</h2>
    <img class="Cartimage" v-bind:src="img" v-bind:alt="img" />
    <h3 class="Cartprice">${{ price }}</h3>
    <h3 class="CartHabitat">{{ Habitat }}</h3>
    <h3 class="Cartdangerous">{{ dangerous }}</h3>
    <h3 class="CartInStock">{{ InStock }}</h3>
    <button @click="removefromShoppingCart" class="Remove">Remove from Cart</button>
  </div>
</template>
