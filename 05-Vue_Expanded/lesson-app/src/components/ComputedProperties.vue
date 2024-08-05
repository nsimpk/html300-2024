<script setup>
import { computed } from 'vue'
const data = {
  firstName: 'John',
  lastName: 'Doe',
  message: 'Hello, World!'
}

const fullName = computed(() => {
  return data.firstName + ' ' + data.lastName
})

const reversedMessage = computed(() => {
  return data.message.split('').reverse().join('')
})
</script>

<template>
  <div>
    <h1>{{ fullName }}</h1>
    <p>{{ reversedMessage }}</p>
  </div>
</template>
