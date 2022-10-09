<script setup>
import PriceItem from "@/components/PriceItem.vue";
const props = defineProps(["prices"]);
</script>

<template>
  <ul class="price-list">
    <PriceItem v-for="(price, idx) in props.prices" :key="idx" :price="price" />
  </ul>
</template>

<style scoped>
.price-list {
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}
</style>
