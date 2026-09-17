<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
function increment() {
  count.value++
}
function decrement() {
  count.value--
}
</script>

<template>
  <main class="counter-page">
      <div class="count" >{{ count }}</div>
      <div class="controls">
        <button class="counter-button"  @click="increment">
          +
        </button>
        <button class="counter-button counter-button--primary"  @click="decrement">
          -
        </button>
      </div>
     
   
  </main>
</template>

<style scoped>
.counter-page {
  min-height: 100vh;
  display: grid;
  place-items: center;
  padding: 2rem;
  background: #f3f0e8;
}

.counter {
  width: min(100%, 34rem);
  padding: 3.5rem 2rem;
  text-align: center;
  color: #263238;
  background: #fffdf8;
  border: 1px solid #d8d2c5;
  border-radius: 1.5rem;
  box-shadow: 0 1.5rem 4rem rgb(38 50 56 / 12%);
}

.eyebrow {
  margin: 0 0 0.75rem;
  color: #c2542d;
  font-size: 0.75rem;
  font-weight: 800;
  letter-spacing: 0.14em;
  text-transform: uppercase;
}

h1 {
  margin: 0;
  font-size: clamp(2rem, 7vw, 3.5rem);
  line-height: 1;
}

.count {
  display: block;
  margin: 2.5rem 0;
  color: #c2542d;
  font-size: clamp(5rem, 20vw, 9rem);
  font-weight: 800;
  line-height: 0.9;
}

.controls {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.counter-button {
  width: 4.5rem;
  height: 4.5rem;
  border: 2px solid #263238;
  border-radius: 50%;
  color: #263238;
  background: transparent;
  font-size: 2.25rem;
  line-height: 1;
  cursor: pointer;
  transition: transform 160ms ease, background-color 160ms ease, color 160ms ease;
}

.counter-button:hover {
  transform: translateY(-3px);
  background: #263238;
  color: #fffdf8;
}

.counter-button:focus-visible {
  outline: 3px solid #e1a33a;
  outline-offset: 4px;
}

.counter-button--primary {
  border-color: #c2542d;
  background: #c2542d;
  color: #fffdf8;
}

.counter-button--primary:hover {
  background: #a94424;
}

.hint {
  margin: 2rem 0 0;
  color: #68757a;
  font-size: 0.9rem;
}

@media (max-width: 480px) {
  .counter-page {
    padding: 1rem;
  }

  .counter {
    padding: 2.5rem 1rem;
  }
}
</style>
