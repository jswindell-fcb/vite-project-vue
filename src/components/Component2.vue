<script setup>
// import { ref } from "vue";

// const name = ref("Swindell");
import { name } from "../stores/testStore";

function changeName() {
  name.value = "Gallay - Comp2";
}
</script>

<template>
  <div>
    <span>Comp2 - {{ name }}</span>
    <button @click="changeName">change name</button>
  </div>
</template>

<style scoped>
button {
  background-color: green;
  color: white;
}
</style>
