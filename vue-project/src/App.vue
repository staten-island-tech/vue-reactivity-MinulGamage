<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="headerDIV">
    <h1 class="header">Monkeys For Sale</h1>
  </div>
  <div class="wrapper">
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/shoppingCart">🛒</RouterLink>
    </nav>
  </div>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.headerDIV {
  font-size: 30px;
  font-weight: bold;
  text-align: center;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 3rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
    width: 100vw;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}

body {
  background-color: cadetblue;
}
</style>
