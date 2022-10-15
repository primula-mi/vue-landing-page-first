<script setup>
import FormInputItem from "@/components/FormInputItem.vue";
let props = defineProps(["formData"]);
</script>
<template>
  <form class="form" action="">
    <h3 class="form__title">
      Application for a <span class="form__title-accent">FREE</span> visit
    </h3>
    <ul class="form__list">
      <li
        class="form__item"
        v-for="(input, idx) in props.formData.inputsplacehoder"
        :key="idx"
      >
        <FormInputItem :placeholderText="input.placeholder" />
      </li>
    </ul>
    <button class="form__button" type="submit">Send</button>
  </form>
</template>

<style scoped>
.form {
  background: #fff;
  width: 40%;
  margin-left: 7em;
}
@media (max-width: 769px) {
  .form {
    width: 70%;
    margin: 0;
  }
}
@media (max-width: 480px) {
  .form {
    width: 90%;
  }
}
.form__title {
  padding: 0.7em 2em;
  background: #f5f5f5;
  font-size: 20px;
  font-weight: 700;
  font-family: "Open Sans", "Arial", sans-serif;
}
.form__title-accent {
  color: lightskyblue;
}
.form__list {
  padding: 1em 1.8em;
}
.form__item {
  margin-top: 2em;
  color: #000;
}
.form__item:last-child {
  margin-bottom: 2em;
}
.form__button {
  width: 100%;
  padding: 1em;
  border: none;
  background: lightskyblue;
  color: #2c3e50;
  font-size: 15px;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
