<script setup>
const props = defineProps(["feedback"]);
</script>
<template>
  <li class="feedback-list__item">
    <p class="feedback-list__comment">{{ props.feedback.comment }}</p>
    <div class="feedback-list__person-info">
      <img
        class="feedback-list__person-photo"
        :src="props.feedback.avatarSrc"
        alt=""
      />
      <p class="feedback-list__person-data">
        <span class="feedback-list__person-name">{{
          props.feedback.name
        }}</span>
        <span class="feedback-list__person-career">{{
          props.feedback.career
        }}</span>
      </p>
    </div>
  </li>
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;600;700&display=swap");

.feedback-list__item {
  width: 25%;
  margin: 0 1em;
}
@media (max-width: 769px) {
  .feedback-list__item {
    display: none;
    width: 50%;
  }
}
@media (max-width: 480px) {
  .feedback-list__item {
    width: 90%;
  }
}
@media (max-width: 769px) {
  .feedback-list__item.active {
    display: block;
  }
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
  display: flex;
  align-items: center;
  margin-top: 1.5em;
}
.feedback-list__person-photo {
  width: 5em;
  height: 5em;
  border-radius: 50%;
}
.feedback-list__person-data {
  display: flex;
  flex-direction: column;
  margin-left: 1em;
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
