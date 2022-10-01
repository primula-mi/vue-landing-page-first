<script setup>
const props = defineProps(["description"]);
</script>
<template>
  <div class="reason-item">
    <h2 class="reason-item__subtitle">{{ props.description.subtitle }}</h2>
    <p class="reason-item__text">{{ props.description.paragraph }}</p>
  </div>
</template>

<style scoped>
.reason-item {
  background-repeat: no-repeat;
  background-size: 4em;
  background-position: top center;
  padding-top: 5em;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.reason-item__subtitle {
  margin-bottom: 1em;
  font-size: 15px;
  font-weight: bold;
  font-family: "Open Sans", "Arial", sans-serif;
}
.reason-item__text {
  text-align: center;
  color: #86878b;
  font-size: 14px;
  font-family: "Open Sans", Arial, sans-serif;
}
</style>
