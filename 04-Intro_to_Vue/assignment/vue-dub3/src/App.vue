<script setup>
import { ref, computed } from 'vue'
import Home from './components/vue-Home.vue'
import Accordion from './components/vue-Accordion.vue'
import Grid from './components/vue-Grid.vue'
import Pics from './components/vue-Pics.vue'
import NotFound from './components/vue-Not-Found.vue'

const text = ref(' Interactive Vue Dub TYPE HERE>')

function changeText(event) {
  text.value = event.target.value
}

const hyperlink = ref('#')

const routes = {
  '/': Home,
  '/vue-Accordion': Accordion,
  '/vue-Grid': Grid,
  '/vue-Pics': Pics
}

const currentPath = ref(window.location.hash)
window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'] || NotFound
})
</script>

<template>
  <header>
    <h1>{{ text }}</h1>
    <input v-modeal="text" @input="changeText" />
    <a v-bind:href="hyperlink">{{ hyperlink }}</a>
  </header>

  <main>
    <a href="#/">Home</a> | <a href="#/vue-Pics">Pics</a> |
    <a href="#/vue-Accordion">Accordion</a> | <a href="#/vue-Grid">Grid</a> |
    <a href="#/vue-Not-Found">Broken Link</a>
    <component :is="currentView" />
  </main>
<!-- Not sure why my Click button doesn't work, It seems to react to link clicks in the nav but not button clicks -->
  <footer>Footer of all footers
    <button @click="show=!show">Click Me</button>
    <p v-if="show">SEE ME</p>
    <p v-else>"NOW YOU DONT"</p>
  </footer>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
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
}
</style>
