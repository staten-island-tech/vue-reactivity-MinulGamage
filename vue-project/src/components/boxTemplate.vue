<template>
  <div class="box">
    <h2 class="name">{{ species }}</h2>
    <img class="image" v-bind:src="img" v-bind:alt="img" />
    <h3 class="price">Price: ${{ price }}</h3>
    <h3 class="Habitat">Habitat: {{ Habitat }}</h3>
    <h3 class="dangerous">Danger Level: {{ dangerous }}</h3>
    <h3 class="InStock">{{ InStock }}</h3>
    <button
      @click.self="
        addToShoppingCart({
          name: species,
          image: img,
          price: price,
          count: 1
        })
      "
      class="Buy"
    >
      {{ buttonLabel }}
    </button>
  </div>
</template>

<script>
import { reactive } from 'vue'
export const monkeyItems = reactive([])
export default {
  data() {
    return {
      price: new Intl.NumberFormat('en-US', {
        style: 'currency',
        currency: 'USD'
      })
    }
  },
  name: 'boxTemplate',
  props: {
    species: String,
    img: String,
    price: Number,
    Habitat: String,
    dangerous: String,
    InStock: String,
    buttonLabel: String
  },
  methods: {
    addToShoppingCart(object) {
      monkeyItems.push(object)
      console.log(monkeyItems)
    }
  }
}
</script>
