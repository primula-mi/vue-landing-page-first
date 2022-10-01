<script setup>
import ReasonItem from "@/components/ReasonItem.vue";
const props = defineProps(["itemList"]);
</script>
<template>
  <ul class="reason-list">
    <li
      class="reason-list__item"
      v-for="(item, idx) in props.itemList"
      :key="idx"
    >
      <ReasonItem
        :description="item"
        :style="{ backgroundImage: `url(${item.imgSrc})` }"
      />
    </li>
  </ul>
</template>

<style scoped>
.reason-list {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 4em;
}
.reason-list__item {
  margin: 0 1em;
}
</style>
