<script setup>
import TabItem from "@/components/TabItem.vue";
import DescriptionItem from "@/components/DescriptionItem.vue";
// import {ref} from "vue";
let props = defineProps(["tabs", "descriptions"]);
// let tabs = ref(props.descriptions);
// let descriptions = ref(props.descriptions);
function selectTab(index) {
  props.tabs.forEach((tab, idx) => {
    tab.isActive = idx === index;
  });
  props.descriptions.forEach((desc, idx) => {
    desc.isActive = idx === index;
  });
}
</script>
<template>
  <div class="tabs-container">
    <ul class="tabs-list">
      <li
        class="tabs-list__item"
        v-for="(tab, idx) in props.tabs"
        :key="tab.text"
        @click="selectTab(idx)"
        :class="{ 'is-active': tab.isActive }"
      >
        <TabItem :text="tab.text" />
      </li>
    </ul>
    <ul class="descriptions-list">
      <li
        class="descriptions-list__item"
        v-for="(description, idx) in props.descriptions"
        :key="idx"
        v-show="description.isActive"
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
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-left: 6em;
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
/* .descriptions-list__item {
  display: none;
}
.descriptions-list__item.is-active {
  display: block;
} */
.tabs-list__item.is-active .box {
  background: lightskyblue;
  /* color: #2c3e50; */
}
</style>
