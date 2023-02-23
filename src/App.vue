<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Cabecera from './components/Cabecera.vue'
</script>

<template>
  <Cabecera/>
  <div class="font-style: italic bg-emerald-600 w-500 h-300 flex font-bold text-5xl">
    <div class="text-left w-1/3 m-4">
    <RouterLink to="/">Inicio</RouterLink> </div>
    <div class="text-center w-1/3 m-4">
    <RouterLink to="/personajes">¿Acerca de nosotros?</RouterLink> </div>
    <div class="text-right w-1/3 m-4">
    <RouterLink to="/about">Personajes</RouterLink> </div>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
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

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
