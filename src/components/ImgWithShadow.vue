<script setup>
const props = defineProps(["imgSrc"]);
</script>

<template>
  <img class="img-with-shadow" :src="props.imgSrc" />
</template>

<style scoped>
.img-with-shadow {
  width: 45%;
  box-shadow: 0 0 15px 0px #777;
}
</style>
