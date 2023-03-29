<template>
  <div class="box">
    <h2 class="name">{{ species }}</h2>
    <img src="{{ Img }}" alt="Image of Monkey" />
    <h3 class="price">{{ price }}</h3>
    <h3 class="Habitat">{{ Habitat }}</h3>
    <h3 class="dangerous">{{ dangerous }}</h3>
    <h3 class="InStock">{{ InStock }}</h3>
    <button class="Buy">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: 'boxTemplate',
  props: {
    species: String,
    img: String,
    price: Number,
    Habitat: String,
    dangerous: String,
    InStock: Boolean
  }
}
</script>
