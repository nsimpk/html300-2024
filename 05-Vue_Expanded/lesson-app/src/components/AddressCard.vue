<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  name: {
    type: String,
    required: true
  },
  address: String,
  phoneNumber: {
    type: String,
    default: '555-555-5555'
  }
})
</script>

<template>
  <div class="address-card">
    <h2>{{ props.name }}</h2>
    <p>{{ props.address }}</p>
    <p>{{ props.phoneNumber }}</p>
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
