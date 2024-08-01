<script setup>
import { ref } from 'vue'

const name = ref('Doug Realguy')

import AddressCard from './components/AddressCard.vue'
</script>

<template>
  <main>
    <h1>Using the AddressCard Component</h1>
    <input type="text" v-model="name" />
    <AddressCard address="432 Mountain Rd" phoneNumber="555-555-5555" />
    <AddressCard name="Jane RealPerson" address="2345 Valley Rd" />
  </main>
</template>

<style scoped>
.address-card {
  background-color: #f5f5f5;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  color: #222;
  width: 300px;
}

h2 {
  font-weight: bold;
}
</style>
