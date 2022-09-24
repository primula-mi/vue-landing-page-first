<script setup>
import FormInputItem from "@/components/FormInputItem.vue";
let forminputs = [
  { placeholder: "Name" },
  { placeholder: "Email" },
  { placeholder: "Password" },
];
</script>
<template>
  <form class="form" action="">
    <h3 class="form__title">
      Try Your <span class="form__title--color">FREE</span> Trial Today
    </h3>
    <ul class="form__list">
      <li
        class="form__item"
        v-for="input in forminputs"
        :key="input.placeholder"
      >
        <FormInputItem :placeholderText="input.placeholder" />
      </li>
    </ul>
    <button class="form__button" type="submit">Get Started</button>
  </form>
</template>

<style scoped>
.form {
  background: #fff;
  width: 40%;
  margin-left: 7em;
}
.form__title {
  padding: 0.7em 2em;
  background: #f5f5f5;
  font-size: 20px;
  font-weight: 700;
  font-family: "Open Sans", "Arial", sans-serif;
}
.form__title--color {
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
