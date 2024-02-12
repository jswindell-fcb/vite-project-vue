<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import NumberWordListing from "./components/NumberWordListing.vue";
import Component1 from "./components/Component1.vue";
import Component2 from "./components/Component2.vue";

import { ref, computed } from "vue";
const num = ref(44);
const nums = [1, 2, 3, 4, 5];
const c = computed(() => nums.reduce((tot, num) => tot + num));
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
  <NumberWordListing></NumberWordListing>
  <Component1 :prop1="c"></Component1>
  <Component2></Component2>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
