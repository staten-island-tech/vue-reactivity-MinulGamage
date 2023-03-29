<script>
import { monkeys } from '../array'
import boxTemplate from '../components/boxTemplate.vue'
export default {
  components: {
    boxTemplate
  },
  data() {
    return {
      monkeys
    }
  }
}
</script>

<template>
  <h1 class="header">Monkeys For Sale</h1>
  <div>
    <boxTemplate
      v-for="monkey in monkeys"
      v-bind:key="monkey"
      :species="monkey.species"
      :img="monkey.img"
      :price="monkey.price"
      :Habitat="monkey.Habitat"
      :dangerous="monkey.dangerous"
    />
  </div>
</template>
