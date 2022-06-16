<script setup>

  import { ref } from 'vue'
  const stamina = ref(10)
  function increment() {
    stamina.value += 1.0
  }
  function decrement() {
    stamina.value -= .08
  }
</script>

<template>
  <main>
    <h1>Stamina: {{stamina.toFixed(1)}}</h1>
    <div class="button-container">
      <button @click="increment">Increment</button>
      <button @click="decrement">Decrement</button>
    </div>
  </main>
</template>

<style scoped>
  .button-container {
    display: flex;
    gap:2%;
  }

  main {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>
