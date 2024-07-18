<script setup>
import {watch, computed, ref} from 'vue'

let count = ref(0)
let count2 = ref(0)
let word = ref("Positif")

function wordMethod() {
  console.log("In method.")
  return count.value < 0 ? "Negatif" : "Positif"
}

// permet de créer une variable dépendante d'une autre variable
const wordComputed = computed(() => {
  console.log("In computed.")
  return count.value < 0 ? "Negatif" : "Positif"
})

// watcher : dans le cas ou j'ai besoin d'un traitement asynchrone dans les computed properties
const counter = watch(count, (newValue, oldValue) => {
  word.value = count.value < 0 ? "Negatif" : "Positif"
  console.log(`Count changed from ${oldValue} to ${newValue}.`)
})

</script>

<template>
  <main>
    <button @click="count++">Increase</button>
    <button @click="count--">Decrease</button>
    <button @click="count2++">Increase 2</button>
    <h1>{{ count }}</h1>
    <h4>{{ wordMethod() }} - {{ wordComputed }} - {{ word }}</h4>
    <h1>{{ count2 }}</h1>
  </main>
</template>