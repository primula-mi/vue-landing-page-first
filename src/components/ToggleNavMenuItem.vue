<script setup>
const props = defineProps(["itemData"]);
</script>
<template>
  <li class="toggle-menu__item">
    <a class="toggle-menu__link" :href="props.itemData.href">{{
      props.itemData.title
    }}</a>
  </li>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");
.toggle-menu__item {
  text-align: center;
  padding-top: 1em;
}
.toggle-menu__link {
  display: inline-block;
  width: 100%;
  color: #fff;
  font-size: 14px;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
