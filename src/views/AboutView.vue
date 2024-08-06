<script setup>
import { useCounterStore } from "@/stores/counter"
const counter = useCounterStore()
const increment = () => {
  counter.$patch((state) => {
    state.count++
  })
}

const decrement = () => {
  counter.$patch((state) => {
    state.count--
  })
}

const resets = () => {
  counter.$patch((state) => {
    state.count = 0
  })
}

import { computed } from 'vue';
// import TheWelcome from '../components/TheWelcome.vue'

const counterStore = useCounterStore()

const counterValue = computed(() => counterStore.count)
</script>
<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button :disabled="counterValue == 0" @click="decrement">-</button>
    <span
      style="width: 20px; height: 20px; display: flex; justify-content: center; align-items: center; background: red;">{{
      counterValue }}</span>
    <button :disabled="counterValue == 10" @click="increment">+</button>
    <button @click="resets">resets</button>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
