<script setup>
const props = defineProps(["itemData"]);
</script>
<template>
  <li class="nav-menu__item">
    <a class="nav-menu__link" :href="props.itemData.href">{{
      props.itemData.title
    }}</a>
  </li>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");
.nav-menu__item {
  margin-left: 4em;
}
.nav-menu__link {
  color: #fff;
  font-size: 14px;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
