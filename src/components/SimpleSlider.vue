<template>
  <div class="slider">
    <button class="prev">ᐊ</button>
    <slot></slot>
    <button class="next">ᐅ</button>
  </div>
</template>
<style scoped>
.prev,
.next {
  display: none;
}
@media (max-width: 769px) {
  .prev,
  .next {
    display: block;
  }
}
</style>
