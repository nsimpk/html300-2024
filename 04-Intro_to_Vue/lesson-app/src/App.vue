<script setup>
import { ref } from "vue";

const show = ref(true);
</script>
<template>
  <main>
    <button @click="show = !show">Toggle paragraph visibility</button>
    <p v-if="show">Can you see me</p>
    <p v-else>Can you this instead?</p>
  </main>
</template>

<style scoped></style>
