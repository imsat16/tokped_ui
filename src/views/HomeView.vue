<template>
  <main>
    <section class="flex">
      <button :disabled="counter === 0" @click="decrement">-</button>
      <input
        style="width: 20px; height: 20px; display: flex; justify-content: center; align-items: center; background: red;"
        v-model="counter" />
      <button :disabled="counter === 10" @click="increment">+</button>
      <button @click="resets">resets</button>
    </section>
  </main>
</template>

<script>
import { computed } from 'vue';
import { useCounterStore } from '@/stores/counter';

export default {
  name: 'CounterComponent', // Optional component name
  setup() {
    const counterStore = useCounterStore();

    const counter = computed({
      get() {
        return counterStore.count;
      },
      set(value) {
        counterStore.$patch({ count: value });
      },
    });

    // const increment = () => {
    //   counter.value++;
    // };

    // const decrement = () => {
    //   counter.value--;
    // };



    return {
      counter,
      // increment,
      // decrement,
    };
  },
  methods: {
    increment() {
      this.counter++;
    },
    decrement() {
      this.counter--;
    },
    resets() {
      this.counter = 0;
    }
  },
};
</script>
