<script setup>
import SubInfoItem from "@/components/SubInfoItem.vue";
const props = defineProps(["subList"]);
</script>

<template>
  <ul class="sub-list">
    <SubInfoItem
      v-for="(item, idx) in props.subList"
      :key="idx"
      :subItem="item"
    />
  </ul>
</template>
