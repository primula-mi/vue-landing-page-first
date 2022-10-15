<script setup>
const props = defineProps(["item"]);
</script>
<template>
  <li class="reason-list__item">
    <h2 class="reason-list__subtitle">{{ props.item.subtitle }}</h2>
    <p class="reason-list__text">{{ props.item.paragraph }}</p>
  </li>
</template>
<style scoped>
.reason-list__item {
  width: 30%;
  margin: 0 1em;
  background-repeat: no-repeat;
  background-size: 4em;
  background-position: top center;
  padding-top: 5em;
  display: flex;
  flex-direction: column;
  align-items: center;
}
@media (max-width: 769px) {
  .reason-list__item {
    display: none;
    width: 50%;
  }
}
@media (max-width: 480px) {
  .reason-list__item {
    width: 100%;
  }
}
@media (max-width: 769px) {
  .reason-list__item.active {
    display: flex;
  }
}
.reason-list__subtitle {
  margin-bottom: 0.8em;
  font-size: 20px;
  font-weight: bold;
  font-family: "Open Sans", "Arial", sans-serif;
}
.reason-list__text {
  text-align: center;
  color: #86878b;
  font-size: 14px;
  font-family: "Open Sans", Arial, sans-serif;
}
</style>
