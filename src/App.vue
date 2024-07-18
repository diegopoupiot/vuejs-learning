<script setup>
import { ref } from 'vue'

let count = ref(0)
let tagname = ref('')

function handleKeyup(event) {
  if (event.code === 'Space') {
    alert('une touche')
  }
}

function increase(step, e) {
  count.value += step
  tagname.value = e.target.tagName
}

function hover(event) {
  tagname.value = event.target.tagName
}

function stopHover(e) {
  e.stopPropagation()
}
</script>

<template>
  <main>
    <h1>{{ count }}</h1>
    <button @click="increase(4, $event)">Increase</button>
    <h2 @mouseover="hover">test</h2>
    <h3 @mouseover.stop="">test</h3>
    <p @mouseover="hover">
      lorem ipsum dolor sit amet <br/>
      Balise : {{ tagname }}
    </p>
    <input type="text" @keyup="handleKeyup">
  </main>
</template>