<script>
import { monkeyItems } from './boxTemplate.vue'
export default {
  name: 'CartBox',
  props: {
    species: String,
    img: String,
    price: Number,
    buttonLabel: String
  },
  methods: {
    removefromShoppingCart(object) {
      console.log(object)
      let box = monkeyItems.find((monkey) => monkey.species === object.species)
      console.log(box)
      console.log(box.count)
      if (box.count > 1) {
        box.count - 1
      } else {
        monkeyItems.splice(box, 1)
      }
    }
  }
}
</script>

<template>
  <div class="CartBox">
    <h2 class="name">{{ species }}</h2>
    <img class="image" v-bind:src="img" v-bind:alt="img" />
    <h3 class="price">Price: ${{ price }}</h3>
    <button @click="removefromShoppingCart({ species: species })" class="Remove">
      Remove from Cart
    </button>
  </div>
</template>
