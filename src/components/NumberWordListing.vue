<script setup>
import { ref, computed, watch } from "vue";

const list = ref(["first", "second", "third", "fourth", "fifth"]);

function updateList() {
  list.value = [...list.value, "new value"];
}

const filteredList = computed(() => {
  console.log("computed - filteredList");
  return list.value.filter((x) => x.includes("new"));
});

watch(filteredList, function (newList, oldList) {
  console.log({ newList, oldList });
});
</script>

<template>
  <button type="button" @click="updateList">Update List</button>
  <div style="display: flex">
    <pre style="width: 50%">{{ list }}</pre>
    <pre style="width: 50%">{{ filteredList }}</pre>
  </div>
</template>
