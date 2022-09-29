<script setup>
let props = defineProps(["text"]);
</script>
<template>
  <div class="box">{{ props.text }}</div>
</template>

<style scoped>
.box {
  padding: 2.2em;
  background: #333333;
  color: #fff;
  transition: all 0.5s ease;
  font-size: 15px;
  font-weight: 700;
  font-family: "Open Sans", "Arial", sans-serif;
}
.box:hover {
  background: #777777;
  /* color: #2c3e50; */
}
</style>
