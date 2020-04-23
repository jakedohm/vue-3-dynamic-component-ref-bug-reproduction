<template>
  <div id="app">
    <div>Count is: {{ count }}</div>

    <Heading as="h1">Count is: {{ count }}</Heading>

    <button @click="increment">Increment</button>
  </div>
</template>

<script>
import { ref } from "vue"
import Heading from "./components/Heading"

export default {
  components: {
    Heading,
  },
  setup() {
    const count = ref(0)
    function increment() {
      count.value++
    }

    return { count, increment }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
