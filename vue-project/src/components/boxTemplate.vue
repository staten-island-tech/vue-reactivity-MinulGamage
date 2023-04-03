<template>
  <div class="box">
    <h2 class="name">{{ species }}</h2>
    <img class="image" v-bind:src="img" v-bind:alt="img" />
    <h3 class="price">${{ price }}</h3>
    <h3 class="Habitat">{{ Habitat }}</h3>
    <h3 class="dangerous">{{ dangerous }}</h3>
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
export const monkeys = reactive([])
export default {
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
      monkeys.push(object)
    }
  }
}
</script>
