<script setup>
defineProps(["paragraph"]);
</script>
<template>
  <p>
    {{ paragraph }}
  </p>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;600;700&display=swap");
p {
  color: #86878b;
}
</style>
