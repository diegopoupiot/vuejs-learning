<script setup>
import {ref} from "vue";

let people = ref([
      {
        id: 1,
        name: "John Doe",
        age: 30
      },
      {
        id: 2,
        name: "Jane Doe",
        age: 25
      },
      {
        id: 3,
        name: "Jim Doe",
        age: 40
      },
      {
        id: 4,
        name: "Jill Doe",
        age: 35
      },
      {
        id: 5,
        name: "Jack Doe",
        age: 20
      }
    ]
);

</script>

<template>
  <main>
    <template v-for="myObject in people" :key="name">
      <h1 v-for="(value, key) in myObject" :key="key">{{ key }}: {{ value }}</h1>
    </template>
  </main>
</template>
