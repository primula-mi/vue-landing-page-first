<script setup>
const props = defineProps(["price"]);
</script>

<template>
  <li class="price-list__item">
    <h4 class="price-list__title">{{ props.price.title }}</h4>
    <p class="price-list__cost">
      $<span>{{ props.price.cost }}</span>
    </p>
    <p class="price-list__subtitle">{{ props.price.subtitle }}</p>
    <p class="price-list__special-subtitle">
      {{ props.price.specialSubtitle ? props.price.specialSubtitle : "" }}
    </p>
    <ul class="price-list__features-list">
      <li
        class="price-list__features-item"
        v-for="(feature, idx) in props.price.features"
        :key="idx"
      >
        {{ feature }}
      </li>
    </ul>
  </li>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;600;700&display=swap");

.price-list__item {
  width: 30%;
  margin: 0 1em;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #333;
  color: #fff;
  font-family: "Open Sans", "Arial", sans-serif;
}
@media (max-width: 769px) {
  .price-list__item {
    display: none;
    width: 50%;
  }
}
@media (max-width: 480px) {
  .price-list__item {
    width: 90%;
  }
}
@media (max-width: 769px) {
  .price-list__item.active {
    display: flex;
  }
}
.price-list__title {
  width: 100%;
  padding: 0.8em 0;
  border-bottom: 1px solid #fff;
  line-height: 20px;
  font-size: 20px;
  font-weight: bold;
  text-align: center;
}
.price-list__cost {
  padding-top: 0.5em;
  padding-bottom: 0.6em;
  font-size: 26px;
  font-weight: bold;
  text-align: center;
  font-family: "Raleway", "Arial", sans-serif;
}
.price-list__cost span {
  font-weight: bold;
  font-size: 72px;
  line-height: 72px;
}
.price-list__subtitle {
  padding-bottom: 1.3em;
  color: #939393;
  line-height: 14px;
  font-size: 14px;
  font-weight: 600;
  font-style: italic;
  font-family: "Open Sans", "Arial", sans-serif;
}
.price-list__special-subtitle {
  width: 100%;
  padding: 0.2em 0;
  background: lightblue;
  color: #333;
  text-align: center;
  line-height: 30px;
  font-size: 14px;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
.price-list__features-list {
  width: 100%;
  background: #fff;
  color: #939393;
  text-align: center;
}
.price-list__features-item {
  padding: 0.2em 0;
  border-bottom: 1px solid #f5f5f5;
  text-transform: uppercase;
  font-size: 14px;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
