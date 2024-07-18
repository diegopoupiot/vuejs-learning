<script setup>
import {ref} from "vue";

  let show = ref(true)
  let color = ref("red")

  //v-show constamment rendu en html alors que pas le v-if
</script>

<template>
  <main>
    <p v-if="show">Hello World</p>
    <h1 v-else-if="color === 'red'">C'est du rouge</h1>
    <h1 v-else>C'est autre chose</h1>
    <button @click="show = !show">Toggle</button>
    <template v-if="show">
      <p>Je suis un paragraphe</p>
    </template>
    <p v-show="show" style="color: red">Je suis un autre paragraphe</p>
  </main>
</template>
