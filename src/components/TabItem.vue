<script setup>
let props = defineProps(["text"]);
</script>
<template>
  <li class="tabs-list__item">
    {{ props.text }}
  </li>
</template>

<style scoped>
.tabs-list__item {
  cursor: pointer;
  padding: 2.2em;
  background: #333333;
  color: #fff;
  transition: all 0.5s ease;
  font-size: 15px;
  font-weight: 700;
  font-family: "Open Sans", "Arial", sans-serif;
}
@media (max-width: 769px) {
  .tabs-list__item {
    padding: 1.5em;
  }
}
@media (max-width: 600px) {
  .tabs-list__item {
    padding: 1em;
  }
}
.tabs-list__item:hover {
  background: #777777;
}
.active,
.active:hover {
  background: lightskyblue;
}
</style>
