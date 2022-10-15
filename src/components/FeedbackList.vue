<script setup>
import FeedbackItem from "@/components/FeedbackItem.vue";
import { ref } from "vue";
const props = defineProps(["feedbacks"]);
let curItem = ref(0);
function prevItem() {
  curItem.value =
    curItem.value - 1 > -1 ? curItem.value - 1 : props.feedbacks.length - 1;
}
function nextItem() {
  curItem.value =
    curItem.value + 1 < props.feedbacks.length ? curItem.value + 1 : 0;
}
</script>

<template>
  <div class="slider">
    <button class="prev" @click="prevItem">
      <span class="arrow arrow--prev"></span>
    </button>
    <ul class="feedback-list">
      <FeedbackItem
        v-for="(feedback, idx) in props.feedbacks"
        :key="idx"
        :class="[curItem === idx ? 'active' : '']"
        :feedback="feedback"
      />
    </ul>
    <button class="next" @click="nextItem">
      <span class="arrow arrow--next"></span>
    </button>
  </div>
</template>

<style scoped>
.feedback-list {
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}
@media (max-width: 769px) {
  .feedback-list {
    justify-content: center;
  }
}
</style>
