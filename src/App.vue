<script setup>
import {computed, ref} from "vue";

  let isBlue = ref(true)
  let isUnderline = ref(true)
  let color = ref('red')
  let size = ref(20)

  const myClass = computed(() => {
    return {
      blue: isBlue.value,
      underline: isUnderline.value,
    }
  })

  const myStyle = computed(() => {
    return {
      color: color.value,
      fontSize: size.value + 'px'
    }
  })
</script>

<template>
  <main>
    <button @click="isBlue = !isBlue">Toggle color</button>
    <button @click="isUnderline = !isUnderline">Toggle underline</button>
    <h1 :class="[myClass, { red: !isBlue}]">Titre 1</h1>
    <h1 :style=myStyle>Titre 2</h1>
    <h1 :class=color>Titre 3</h1>
    <input type="text" v-model="color">
    <input type="text" v-model="size">
  </main>
</template>