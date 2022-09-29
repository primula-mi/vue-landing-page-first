<script setup>
import Logo from "@/components/LogoItem.vue";
import HeaderNavMenu from "@/components/HeaderNavMenu.vue";
</script>

<template>
  <header>
    <div class="container">
      <Logo />
      <HeaderNavMenu />
    </div>
    <!-- <div class="wrapper"></div> -->
  </header>
</template>

<style scoped>
header {
  background: #1c1f24;
}
header .container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  padding: 0.5em 0;
}
</style>
