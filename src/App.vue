<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value = count.value + 1
}
function decrement() {
  count.value = count.value - 1
}
</script>

<template>
  <main class="counter-page">
    <div class="counter-card">
      <h1>Mon compteur</h1>
      <p class="count">{{ count }}</p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </div>
  </main>
</template>

<style scoped>
.counter-page {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f0f0f0;
}

.counter-card {
  background-color: white;
  padding: 40px;
  border-radius: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
  text-align: center;
}

h1 {
  color: #333;
}

.count {
  font-size: 80px;
  color: orangered;
  font-weight: bold;
}

button {
  font-size: 30px;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  border: none;
  background-color: orangered;
  color: white;
  margin: 10px;
  cursor: pointer;
}
</style>