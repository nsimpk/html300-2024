<script setup>
import { ref } from 'vue'

const name = ref('Pics')

const images = ref(["Dog Image", "Painting Image"])
</script>

<template>
  <h1>PICS</h1>
  <ul>
    <li v-for="image in images" :key="image">
      {{ image }}
    </li>
<!-- Need to add these images to the above array -->
    <picture>
      <source>
        <img src="../assets/images/this_is_fine.jpg" class="img-fluid" alt="this is fine">
        <img src="../assets/images//PNW.jpg" class="img-fluid" alt="PNW">
    </picture>
  </ul>
</template>

<style scoped>
.pics {
  text-align: center;
  margin-top: auto;
}
</style>
