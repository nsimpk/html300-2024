<script setup>
import { ref } from "vue";

const text = ref("Hello!");

function changeText(event) {
  text.value = event.target.value;
}
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="./assets/logo.svg"
      width="125"
      height="125"
    />
    <h1>{{ text }}</h1>
    <!-- v-on syntax example: -->
    <!-- <input v-model="text" v-on:input="changeText" /> -->

    <!-- @ syntax example: -->
    <input v-model="text" @input="changeText" />
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
}
</style>
