<template>
  <div class="counter">
    <h1 class="green">Counter</h1>
    <div class="divider">
      <button class="button" @click="counterStore.add()">Add</button>
      <button class="button" @click="counterStore.reset()">Reset</button>
      <button class="button" @click="counterStore.subtract()">Subtract</button>
    </div>
    <h2>The value is: {{ counterStore.count }}</h2>
  </div>
</template>

<script setup lang="ts">
import { useCounterStore } from "@/stores/counter";
const counterStore = useCounterStore();
</script>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
}

.counter {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.divider {
  padding: 1rem;
}

.button {
  margin-left: 10px;
  margin-right: 10px;
  min-width: 100px;
  min-height: 100px;
  font-weight: bold;
  border-radius: 50%;
}
</style>