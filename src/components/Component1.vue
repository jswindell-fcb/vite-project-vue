<script setup>
import { ref } from "vue";

const props = defineProps({
  prop1: {
    type: Number,
    required: true
  }
});

console.log(props.prop1);
console.log(typeof props.prop1);

// const name = ref("Swindell");
import { name } from "../stores/testStore";

function changeName() {
  name.value = "Gallay";
}

</script>

<template>
  <div>
    <span>Comp1 - {{ name }}</span>
    <button @click="changeName">change name</button>
  </div>
</template>

<style scoped>
button {
  background-color: blue;
  color: white;
}
</style>
