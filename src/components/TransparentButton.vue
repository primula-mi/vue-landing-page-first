<script setup>
let props = defineProps(["buttonText"]);
</script>
<template>
  <a class="transparent-btn" href="#">{{ props.buttonText }}</a>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");
.transparent-btn {
  display: block;
  padding: 0.7em 2.2em;
  border: 2px solid #fff;
  background: none;
  color: #fff;
  font-size: 15px;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
