<script setup>
const props = defineProps(["feedback"]);
</script>
<template>
  <li class="feedback-list__item">
    <p class="feedback-list__comment">{{ props.feedback.comment }}</p>
    <div
      class="feedback-list__person-info"
      :style="{ backgroundImage: `url(${props.feedback.avatarSrc})` }"
    >
      <p class="feedback-list__person-name">{{ props.feedback.name }}</p>
      <p class="feedback-list__person-career">{{ props.feedback.career }}</p>
    </div>
  </li>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;600;700&display=swap");

.feedback-list__item {
  max-width: 26%;
}
.feedback-list__comment {
  padding: 1.5em 1em;
  background: #f5f5f5;
  font-size: 14px;
  font-style: italic;
  font-family: "Open Sans", "Arial", sans-serif;
}
.feedback-list__comment:after {
  content: "";
  position: absolute;
  top: 100%;
  left: 13%;
  transform: translateX(-50%);
  display: block;
  width: 0;
  height: 0;
  border-left: 12px solid transparent;
  border-right: 12px solid transparent;
  border-top: 18px solid #f5f5f5;
}
.feedback-list__person-info {
  margin-top: 1.5em;
  padding: 1em 0 1em 6em;
  background-repeat: no-repeat;
  background-size: 5em;
  background-position: left center;
}
.feedback-list__person-name {
  font-size: 20px;
  font-weight: bold;
  font-family: "Open Sans", "Arial", sans-serif;
}
.feedback-list__person-career {
  color: #86878b;
  font-size: 14px;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
