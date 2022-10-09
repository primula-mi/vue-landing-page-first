<script setup>
import FormInputItem from "@/components/FormInputItem.vue";
let forminputs = [
  { placeholder: "Name" },
  { placeholder: "Email" },
  { placeholder: "Subject" },
];
</script>
<template>
  <form class="form" action="">
    <div class="form__content">
      <ul class="form__list">
        <li
          class="form__item"
          v-for="input in forminputs"
          :key="input.placeholder"
        >
          <FormInputItem :placeholderText="input.placeholder" />
        </li>
      </ul>
      <textarea
        name=""
        id=""
        cols="30"
        rows="7"
        placeholder="Message"
      ></textarea>
    </div>
    <button class="form__button" type="submit">Send Message</button>
  </form>
</template>
<style scoped>
.form {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.form__content {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin: 4em 0 3em;
}
.form__list {
  width: 47%;
}
.form__item {
  margin-top: 2em;
  color: #000;
}
.form__button {
  padding: 1em;
  border: none;
  background: lightskyblue;
  color: #2c3e50;
  font-size: 15px;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
textarea {
  width: 47%;
  border: none;
  border-bottom: 1px solid #d6d6d6;
  font-size: 14px;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>
