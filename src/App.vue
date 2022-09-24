<script setup>
import HeaderItem from "@/components/HeaderItem.vue";
import Logo from "@/components/LogoItem.vue";
import DescriptionItem from "@/components/DescriptionItem.vue";
import FormMainPage from "@/components/FormMainPage.vue";
let descriptions = {
  mainPage: {
    subtitle: {
      text: "Modern axure template for beautiful prototypes",
      style: {
        color: "#fff",
        fontSize: 36,
        fontFamily: "Raleway",
      },
    },
    paragraph: {
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo.",
      style: {
        size: 16,
        fontFamily: "Raleway",
      },
    },
  },
};
</script>

<template>
  <HeaderItem />
  <main>
    <section class="main-page">
      <div class="container">
        <div class="description">
          <Logo />
          <DescriptionItem
            :subtitle="descriptions.mainPage.subtitle"
            :paragraph="descriptions.mainPage.paragraph"
          />
        </div>
        <FormMainPage />
      </div>
    </section>
  </main>
</template>

<style scoped>
.main-page {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #7c7c7c url(@/assets/img/banner-main.jpg) no-repeat center/cover;
  background-blend-mode: multiply;
}
.description {
  width: 60%;
  margin-right: 9em;
}
</style>
