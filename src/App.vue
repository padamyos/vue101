<script setup>

import { reactive } from 'vue'
const counter = reactive({ count: 0 })
const increment = () => {
  counter.count++
}
const GotoGoogle = () => {
  window.location.href = 'https://www.google.com'
}
</script>

<template>
  <div>
    <nav>
      <h1 class="text-2xl p-5">
        counter: {{ counter.count }}
      </h1>
      <button @click="increment" class="bg-purple-700 text-white p-5 rounded-xl">Increment</button>
      <button @click="GotoGoogle" class="bg-purple-700 text-white p-5 rounded-xl">Go to google</button>
      <RouterLink to="/about" class="p-10 bg-purple-800 text-white">Go to About</RouterLink>
    </nav>
    <main>
      <RouterView />

    </main>
  </div>

</template>

<style></style>