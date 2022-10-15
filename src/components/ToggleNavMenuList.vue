<script setup>
import ToggleNavMenuItem from "@/components/ToggleNavMenuItem.vue";
const props = defineProps(["navMenuItems"]);
</script>
<template>
  <nav class="toggle-menu__nav">
    <ul class="toggle-menu__list">
      <ToggleNavMenuItem
        v-for="(item, idx) in props.navMenuItems"
        :key="idx"
        :itemData="item"
      />
    </ul>
  </nav>
</template>

<style scoped>
.toggle-menu__nav {
  position: fixed;
  top: 62px;
  bottom: 0;
  right: -100%;
  z-index: 4;
  width: 100%;
  background: #1c1f24;
  transition: all 0.4s ease;
}
.toggle-menu__nav.active {
  right: 0;
}
.toggle-menu__list {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
