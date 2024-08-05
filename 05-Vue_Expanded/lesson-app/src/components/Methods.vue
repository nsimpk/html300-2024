<script setup>
const getHeadlineMessage = (name) => {
  return `Hello, ${name}!`
}
</script>

<template>
  <div>
    <h1>{{ getHeadlineMessage('Kevin') }}</h1>
  </div>
</template>
