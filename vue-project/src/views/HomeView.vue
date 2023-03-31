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
  <div class="Parent-Box">
    <boxTemplate
      v-for="monkey in monkeys"
      v-bind:key="monkey"
      :species="monkey.species"
      :img="monkey.img"
      :price="monkey.price"
      :Habitat="monkey.Habitat"
      :dangerous="monkey.dangerous"
      :InStock="monkey.InStock"
    />
  </div>
</template>

<style>
.box {
  border: 4px solid black;
  border-radius: 10%;
  width: 30vw;
  height: 70vh;
  margin: 20px auto;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
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
}
.price {
  text-align: center;
}

.Buy {
  text-align: center;
  align-items: center;
  justify-content: center;
}
.Habitat {
  text-align: center;
}
.dangerous {
  text-align: center;
}
.InStock {
  text-align: center;
}
</style>
