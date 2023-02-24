<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import Cabecera from './components/Cabecera.vue'
</script>

<template>
  <Cabecera/>
  <div class="font-mono bg-emerald-600 w-500 h-300 flex font-bold text-5xl border-y-8 border-y-sky-700">
    <RouterLink to="/" class="text-center w-1/3 m-4 hover:border-8 rounded-3xl">Inicio</RouterLink>
    <RouterLink to="/about" class="text-center w-1/3 m-4 hover:border-8 rounded-3xl">Acerca de</RouterLink>
    <RouterLink to="characters" class="text-center w-1/3 m-4 hover:border-8 rounded-3xl">Personajes</RouterLink>
  </div>
  <div class="bg-emerald-200">
  <RouterView />
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
