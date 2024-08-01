<script setup>
import { ref } from 'vue'

const address = ref({
  name: 'Jane Doe',
  address: '1234 Fake St',
  phoneNumber: '555-555-5555'
})
</script>

<template>
  <div class="address-card">
    <h2>{{ address.name }}</h2>
    <p>{{ address.address }}</p>
    <p>{{ address.phoneNumber }}</p>
  </div>
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
