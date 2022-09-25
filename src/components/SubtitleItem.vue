<script setup>
defineProps(["subtitle"]);
</script>
<template>
  <h2>{{ subtitle }}</h2>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;600;700&display=swap");
h2 {
  color: #000;
  font-weight: bold;
}
h2::selection {
  background-color: lightskyblue;
}
</style>
