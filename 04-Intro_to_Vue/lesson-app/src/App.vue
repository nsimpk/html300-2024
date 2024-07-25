<script setup>
import { ref } from "vue";

// Conditional rendering
const show = ref(true);

// Loop over Array
const ingredients = ref(["meat", "cheese", "veggies"]);

// Loop over Array of Objects
const people = ref([
  { name: "John", age: 30 },
  { name: "Jane", age: 25 },
  { name: "Susan", age: 41 },
]);
</script>
<template>
  <main>
    <!-- Conditional rendering -->
    <button @click="show = !show">Toggle paragraph visibility</button>
    <p v-if="show">Can you see me?</p>

    <!-- Loop over Array -->
    <ul>
      <li v-for="ingredient in ingredients" :key="ingredient">
        {{ ingredient }}
      </li>
    </ul>

    <!-- Loop over Array of Objects -->
    <ul>
      <li v-for="person in people" :key="person.name">
        {{ person.name }} is {{ person.age }} years old.
      </li>
    </ul>
  </main>
</template>

<style scoped></style>
