<script setup>
import { ref } from 'vue'

let title = ref('Hello Vite + Vue 3')
let strongMessage = "<i>IMPORTANT</i>"

function reverseTitle() {
  title.value = title.value.split('').reverse().join('')
  console.log('Title reversed:', title.value)
}
</script>

<template>
  <main>
    <h1 v-once>{{ title }}</h1>
    <h1>{{ title }}</h1>
    <h3>{{ title === 'Hello Vite + Vue 3' ? "ok" : "non ok" }}</h3>
    <input type="text" v-model="title">
    <button @click="reverseTitle">Reverse title</button>
    <p v-once :title="title">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non risus. Suspendisse lectus tortor
      <span>
        {{ title }}
      </span>
    </p>
    <p v-html="strongMessage"></p>
  </main>
</template>