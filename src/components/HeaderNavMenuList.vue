<script setup>
import HeaderNavMenuItem from "@/components/HeaderNavMenuItem.vue";
const props = defineProps(["navMenuItems"]);
</script>
<template>
  <nav class="nav-menu">
    <ul class="nav-menu__list">
      <HeaderNavMenuItem
        v-for="(item, idx) in props.navMenuItems"
        :key="idx"
        :itemData="item"
      />
    </ul>
  </nav>
</template>

<style scoped>
.nav-menu {
  width: 100%;
}
.nav-menu__list {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  margin: 0;
  padding: 0;
}
</style>
