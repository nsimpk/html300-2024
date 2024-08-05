<script setup>
import Ternary from './components/Ternary.vue'
import ComputedProperties from './components/ComputedProperties.vue'
import Methods from './components/Methods.vue'
import TernaryWithComposable from './components/TernaryWithComposable.vue'
import SlotChildComponent from './components/SlotChildComponent.vue'
import NamedSlotsComponent from './components/NamedSlotsComponent.vue'
</script>

<template>
  <main>
    <!-- Using Terneray Operator to change the value of counter -->
    <Ternary />
    <!-- Using ComputedProperties to generate values -->
    <ComputedProperties />
    <!-- Using Methods to generate values -->
    <Methods />
    <!-- Using Composable to reuse logic -->
    <TernaryWithComposable />

    <SlotChildComponent>
      <div class="address-card">
        <h2>Address Card</h2>
        <p>123 Main St</p>
        <p>Springfield, IL 62701</p>
      </div>
    </SlotChildComponent>

    <NamedSlotsComponent>
      <template v-slot:header>
        <h2>Header Slot</h2>
      </template>
      <h1>Default Slot</h1>
      <template v-slot:footer>
        <h2>Footer Slot</h2>
      </template>
    </NamedSlotsComponent>
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
