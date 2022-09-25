<script setup>
import TabItem from "@/components/TabItem.vue";
import DescriptionItem from "@/components/DescriptionItem.vue";

let props = defineProps(["tabs", "description"]);
</script>
<template>
  <div class="tabs-container">
    <ul class="tabs-list">
      <li class="tabs-list__item" v-for="tab in props.tabs" :key="tab.text">
        <TabItem :text="tab.text" />
      </li>
    </ul>
    <ul class="descriptions-list">
      <li class="descriptions-list__item">
        <DescriptionItem
          :subtitle="props.description.subtitle"
          :paragraph="props.description.paragraph"
        />
      </li>
    </ul>
  </div>
</template>

<style scoped>
.tabs-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 5em 6em 5em 0;
  width: 75%;
}
.tabs-list {
  width: 15%;
}
.tabs-list__item {
  cursor: pointer;
}
.descriptions-list {
  margin-left: 6em;
  width: 75%;
}
</style>
