<script setup>
import TabItem from "@/components/TabItem.vue";
import DescriptionItem from "@/components/DescriptionItem.vue";
import { ref } from "vue";
let props = defineProps(["tabs", "descriptions"]);
let isActive = ref(0);
</script>
<template>
  <div class="tabs-container">
    <ul class="tabs-list">
      <TabItem
        :text="tab.text"
        v-for="(tab, idx) in props.tabs"
        :key="idx"
        @click="isActive = idx"
        :class="[isActive === idx ? 'active' : '']"
      />
    </ul>
    <ul class="descriptions-list">
      <li
        class="descriptions-list__item"
        v-for="(description, idx) in props.descriptions"
        :key="idx"
        v-show="isActive === idx"
      >
        <DescriptionItem
          :subtitle="description.subtitle"
          :paragraph="description.paragraph"
        />
      </li>
    </ul>
  </div>
</template>

<style scoped>
.tabs-container {
  padding-right: 26em;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
@media (max-width: 769px) {
  .tabs-container {
    justify-content: space-around;
    padding: 0;
  }
}
@media (max-width: 600px) {
  .tabs-container {
    flex-direction: column;
  }
}
.tabs-list {
  width: 15%;
}
@media (max-width: 769px) {
  .tabs-list {
    width: fit-content;
  }
}
@media (max-width: 600px) {
  .tabs-list {
    display: flex;
    margin-bottom: 1em;
  }
}
.descriptions-list {
  width: 75%;
}
@media (max-width: 600px) {
  .descriptions-list {
    width: 95%;
  }
}
</style>
