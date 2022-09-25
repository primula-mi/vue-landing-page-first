<script setup>
import HeaderItem from "@/components/HeaderItem.vue";
import Logo from "@/components/LogoItem.vue";
import DescriptionItem from "@/components/DescriptionItem.vue";
import TransparentButton from "@/components/TransparentButton.vue";
import FormMainPage from "@/components/FormMainPage.vue";
import SubtitleItem from "@/components/SubtitleItem.vue";
import ParagraphItem from "@/components/ParagraphItem.vue";
import SocialMedia from "@/components/SocialMedia.vue";
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
        color: "#fff",
        size: 16,
        fontFamily: "Raleway",
      },
    },
    transparentButton: {
      buttonText: "Download",
    },
  },
  socialMedia: {
    subtitle: {
      text: "Social Media",
      style: {
        color: "#333333",
        fontSize: 20,
        fontFamily: "Open Sans",
      },
    },
    paragraph: {
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet.",
      style: {
        fontSize: 14,
        fontFamily: "Open Sans",
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
        <div class="main-page__description">
          <Logo />
          <DescriptionItem
            :subtitle="descriptions.mainPage.subtitle"
            :paragraph="descriptions.mainPage.paragraph"
          />
          <TransparentButton
            :buttonText="descriptions.mainPage.transparentButton.buttonText"
          />
        </div>
        <FormMainPage />
      </div>
    </section>
    <section class="social-media">
      <div class="container">
        <div class="social-media__description">
          <SubtitleItem
            :subtitle="descriptions.socialMedia.subtitle.text"
            :style="{
              color: `${descriptions.socialMedia.subtitle.style.color}`,
              fontSize: `${descriptions.socialMedia.subtitle.style.fontSize}px`,
              fontFamily: `${descriptions.socialMedia.subtitle.style.fontFamily}, Arial, sans-serif`,
            }"
          />
          <ParagraphItem
            :paragraph="descriptions.socialMedia.paragraph.text"
            :style="{
              fontSize: `${descriptions.socialMedia.paragraph.style.fontSize}px`,
              fontFamily: `${descriptions.socialMedia.paragraph.style.fontFamily}, Arial, sans-serif`,
            }"
          />
        </div>
        <SocialMedia />
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
.main-page__description {
  width: 60%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-right: 9em;
}
.transparent-btn {
  margin-top: 3em;
}
.social-media {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  /* height: 10vh; */
}
.social-media__description {
  width: 40%;
  margin: 1em 0;
}
</style>
