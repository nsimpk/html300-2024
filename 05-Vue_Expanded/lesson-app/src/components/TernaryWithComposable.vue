<script setup>
import { useCounter } from '../composables/useCounter'

const { count, increment, decrement } = useCounter()
</script>

<template>
  <main>
    <div>
      <button @click="increment">Increment</button>
      <button @click="decrement">Decrement</button>
      <p>Counter: {{ count }}</p>
    </div>
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
