<script setup>
import { ref, onMounted } from 'vue'

const apiData = ref(null)
const loading = ref(false)
const errorMessage = ref(null)

onMounted(() => {
  loading.value = true
  fetch('https://jsonplaceholder.typicode.com/users')
    .then((response) => response.json())
    .then((data) => {
      console.log(data)
      apiData.value = data
      loading.value = false
    })
    .catch((error) => {
      console.error('Error:', error)
      loading.value = false
      errorMessage.value = error.message
    })
    .finally(() => {
      console.log('API call completed.')
    })
})
</script>

<template>
  <div>
    <h1>API Lesson</h1>
    <p v-if="loading">Loading...</p>
    <p v-if="errorMessage">Error: {{ errorMessage }}</p>
    <ul>
      <li v-for="user in apiData" :key="user.id">
        <h2>{{ user.name }}</h2>
        <p>{{ user.email }}</p>
      </li>
    </ul>
  </div>
</template>

<style scoped></style>
