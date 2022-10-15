<script setup>
let props = defineProps(["placeholderText"]);
</script>
<template>
  <input type="text" :placeholder="props.placeholderText" />
</template>

<style scoped>
input {
  width: 100%;
  border: none;
  outline: none;
  border-bottom: 1px solid #d6d6d6;
  color: #aaa;
  font-size: 14px;
  font-family: "Open Sans", "Arial", sans-serif;
}
input:focus {
  border-bottom: 1px solid #aaa;
}
</style>
