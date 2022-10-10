<script setup>
import Logo from "@/components/LogoItem.vue";
import HeaderNavMenuList from "@/components/HeaderNavMenuList.vue";
const props = defineProps(["headerData"]);
</script>

<template>
  <header>
    <div class="container">
      <Logo />
      <HeaderNavMenuList :navMenuItems="props.headerData" />
    </div>
  </header>
</template>

<style scoped>
header {
  background: #1c1f24;
  z-index: 5;
}
header .container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  padding: 0.5em 0;
}
</style>
