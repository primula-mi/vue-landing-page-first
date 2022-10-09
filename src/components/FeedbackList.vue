<script setup>
import FeedbackItem from "@/components/FeedbackItem.vue";
const props = defineProps(["feedbacks"]);
</script>

<template>
  <ul class="feedback-list">
    <FeedbackItem
      v-for="(feedback, idx) in props.feedbacks"
      :key="idx"
      :feedback="feedback"
    />
  </ul>
</template>

<style scoped>
.feedback-list {
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}
</style>
