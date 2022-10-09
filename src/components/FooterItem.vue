<script setup>
import SocialMedia from "@/components/SocialMedia.vue";
</script>
<template>
  <footer class="footer">
    <SocialMedia :class="{ small: true }" />
    <p>© 2015 Axure Themes</p>
  </footer>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");

.footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1.5em 0 1em;
  background: #1c1f24;
  color: #fff;
  font-size: 12px;
  font-family: "Open Sans", "Arial", sans-serif;
}
.social-media-icon {
  width: 20%;
  margin: 0 0 0.3em;
}
</style>
