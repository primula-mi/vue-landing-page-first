<script setup>
import PriceItem from "@/components/PriceItem.vue";
import { ref } from "vue";
const props = defineProps(["prices"]);
let curItem = ref(0);
function prevItem() {
  curItem.value =
    curItem.value - 1 > -1 ? curItem.value - 1 : props.prices.length - 1;
}
function nextItem() {
  curItem.value =
    curItem.value + 1 < props.prices.length ? curItem.value + 1 : 0;
}
</script>

<template>
  <div class="slider">
    <button class="prev" @click="prevItem">
      <span class="arrow arrow--prev"></span>
    </button>
    <ul class="price-list">
      <PriceItem
        v-for="(price, idx) in props.prices"
        :key="idx"
        :class="[curItem === idx ? 'active' : '']"
        :price="price"
      />
    </ul>
    <button class="next" @click="nextItem">
      <span class="arrow arrow--next"></span>
    </button>
  </div>
</template>

<style scoped>
.price-list {
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}
@media (max-width: 769px) {
  .price-list {
    justify-content: center;
  }
}
</style>
