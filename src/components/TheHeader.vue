<script setup>
import Logo from "@/components/LogoItem.vue";
import HeaderNavMenuList from "@/components/HeaderNavMenuList.vue";
import TheToggleMenu from "@/components/TheToggleMenu.vue";
const props = defineProps(["headerData"]);
</script>

<template>
  <header>
    <div class="container">
      <Logo />
      <HeaderNavMenuList :navMenuItems="props.headerData" />
      <TheToggleMenu :navMenuItems="props.headerData" />
    </div>
  </header>
</template>

<style scoped>
header {
  background: #1c1f24;
  z-index: 5;
  position: fixed;
  width: 100%;
}
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  padding: 0.5em 0;
}
@media (max-width: 769px) {
  .container {
    padding: 0.5em 1em;
  }
}
</style>
