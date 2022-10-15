<script setup>
import ReasonItem from "@/components/ReasonItem.vue";
import { ref } from "vue";
const props = defineProps(["itemList"]);
let curItem = ref(0);
function prevItem() {
  curItem.value =
    curItem.value - 1 > -1 ? curItem.value - 1 : props.itemList.length - 1;
}
function nextItem() {
  curItem.value =
    curItem.value + 1 < props.itemList.length ? curItem.value + 1 : 0;
}
</script>
<template>
  <div class="slider">
    <button class="prev" @click="prevItem">
      <span class="arrow arrow--prev"></span>
    </button>
    <ul class="reason-list">
      <ReasonItem
        v-for="(item, idx) in props.itemList"
        :key="idx"
        :item="item"
        :class="[curItem === idx ? 'active' : '']"
        :style="{ backgroundImage: `url(${item.imgSrc})` }"
      />
    </ul>
    <button class="next" @click="nextItem">
      <span class="arrow arrow--next"></span>
    </button>
  </div>
</template>

<style scoped>
.reason-list {
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* margin-top: 4em; */
}
</style>
