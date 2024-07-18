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
    <ul>
      <li v-for="n in 10">
        n
      </li>
    </ul>
  </main>
</template>
