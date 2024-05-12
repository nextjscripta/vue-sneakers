<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => {
  console.log(count)
  count.value++
}
</script>

<template>
  <div class="flex size-1/2">
    <h1 class="size-5 accent-amber-100">My name is Dmitry</h1>
    <h2>i'm a frontend developer</h2>
    <p>{{ count }}</p>
    <button @click="increment">Click Me</button>
    <input v-model="count" type="text" />
  </div>
</template>

<style scoped></style>
