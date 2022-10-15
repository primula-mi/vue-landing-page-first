<script setup>
const props = defineProps(["description"]);
</script>
<template>
  <div class="header-center">
    <h2 class="header-center__subtitle">{{ props.description.subtitle }}</h2>
    <svg
      class="header-center__line"
      viewBox="0 0 100 1"
      xmlns="http://www.w3.org/2000/svg"
    >
      <line x1="0" y1="0" x2="30" y2="0"></line>
    </svg>
    <p class="header-center__text">{{ props.description.paragraph }}</p>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;1,400&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;600;700&display=swap");

/* TODO подключить шрифт из макета */
.header-center {
  display: flex;
  align-items: center;
  flex-direction: column;
  margin-bottom: 4em;
}
@media (max-width: 769px) {
  .header-center {
    margin-bottom: 2em;
  }
}
.header-center__subtitle {
  text-align: center;
  text-transform: uppercase;
  font-size: 36px;
  font-family: "Raleway", "Arial", sans-serif;
}
.header-center__line {
  fill: lightskyblue;
  stroke: lightskyblue;
  margin: 1em 0;
  padding-left: 40%;
}
.header-center__text {
  color: #86878b;
  font-size: 14px;
  font-family: "Open Sans", Arial, sans-serif;
}
.colorWhite {
  color: #fff;
}
.colorWhite .header-center__line {
  fill: #fff;
  stroke: #fff;
}
.colorWhite .header-center__text {
  color: #fff;
  font-weight: 300;
}
</style>
