<script setup>
import SubtitleItem from "@/components/SubtitleItem.vue";
import ParagraphItem from "@/components/ParagraphItem.vue";

let props = defineProps(["subtitle", "paragraph"]);
</script>
<template>
  <SubtitleItem
    :subtitle="props.subtitle.text"
    :style="{
      color: `${props.subtitle.style.color}`,
      fontSize: `${props.subtitle.style.fontSize}px`,
      fontFamily: `${props.subtitle.style.fontFamily}, Arial, sans-serif`,
    }"
  />
  <svg class="line" viewBox="0 0 100 1" xmlns="http://www.w3.org/2000/svg">
    <line x1="0" y1="0" x2="20" y2="0"></line>
  </svg>
  <ParagraphItem
    :paragraph="props.paragraph.text"
    :style="{
      fontSize: `${props.paragraph.style.fontSize}px`,
      fontFamily: `${props.paragraph.style.fontFamily}, Arial, sans-serif`,
    }"
  />
</template>

<style scoped>
.line {
  fill: lightskyblue;
  stroke: lightskyblue;
  margin: 1em 0;
}
</style>
