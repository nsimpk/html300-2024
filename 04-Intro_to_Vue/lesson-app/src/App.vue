<script setup>
import { ref } from "vue";

const ingredients = ref(["meat", "cheese", "veggies"]);

const show = ref(true)
</script>
<template>
  <main>
    <button @click='show = !show">Toggle paragraph visibility</button>
    <p v-if='show'>Can you see me?</p>
    <ul>
      <li v-for="ingredient in ingredients" :key="ingredient">
        {{ ingredient }}
      </li>
    </ul>
  </main>
</template>

<style scoped></style>
