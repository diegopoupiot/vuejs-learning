<script setup>
let title = 'Hello Vite + Vue 3'

function reverseTitle() {
  title = title.split('').reverse().join('')
  console.log('Title reversed:', title)
}
</script>

<template>
  <main>
    <h1>{{ title }}</h1>
    <button v-on:click="reverseTitle">Reverse title</button>
  </main>
</template>