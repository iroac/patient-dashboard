<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <div class="router" >
    <RouterView />
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-width: 100vw;
}

.router {
  padding: 0 1rem;
  min-height: 100vh;
  min-width: 100vw;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100vw;
  font-size: 12px;
  background-color: cadetblue;
  text-align: center;
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
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    flex-direction: row;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    display: flex;
    flex-direction: row;
    font-size: 1rem;
    padding: 1rem 0;
  }
}
</style>
