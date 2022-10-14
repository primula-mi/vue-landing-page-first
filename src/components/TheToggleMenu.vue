<script setup>
import ToggleItem from "@/components/ToggleItem.vue";
import ToggleNavMenuList from "@/components/ToggleNavMenuList.vue";
import { ref } from "vue";
let isActive = ref(false);
const props = defineProps(["navMenuItems"]);
</script>
<template>
  <div class="toggle-menu">
    <ToggleItem :class="{ active: isActive }" @click="isActive = !isActive" />
    <ToggleNavMenuList
      :class="{ active: isActive }"
      :navMenuItems="props.navMenuItems"
    />
  </div>
</template>
<style scoped>
.toggle-menu {
  display: none;
}
@media (max-width: 769px) {
  .toggle-menu {
    display: block;
  }
}
</style>
