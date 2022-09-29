<script setup>
const props = defineProps(["subList"]);
</script>

<template>
  <ul class="sub-list">
    <li class="sub-list__item" v-for="(item, idx) in props.subList" :key="idx">
      <h3 class="sub-list__title">{{ item.subTitle }}</h3>
      <p class="sub-list__text">{{ item.text }}</p>
    </li>
  </ul>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");
.sub-list__item {
  background-image: url(/src/assets/img/icon/cat-list-icon.png);
  background-repeat: no-repeat;
  background-size: 3em;
  background-position: left center;
  padding-left: 4em;
  margin: 2em 0;
}
.sub-list__title {
  color: #333;
  font-size: 14px;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
.sub-list__text {
  color: #86878b;
  font-size: 14px;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
