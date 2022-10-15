<script setup>
import TheHeader from "@/components/TheHeader.vue";
import Logo from "@/components/LogoItem.vue";
import DescriptionItem from "@/components/DescriptionItem.vue";
// import TransparentButton from "@/components/TransparentButton.vue";
import FormMainPage from "@/components/FormMainPage.vue";
import SubtitleItem from "@/components/SubtitleItem.vue";
import ParagraphItem from "@/components/ParagraphItem.vue";
import SocialMedia from "@/components/SocialMedia.vue";
// import TabsList from "@/components/TabsList.vue";
import ImgWithShadow from "@/components/ImgWithShadow.vue";
import SubInfoList from "@/components/SubInfoList.vue";
import HeaderCenterPage from "@/components/HeaderCenterPage.vue";
import ReasonList from "@/components/ReasonList.vue";
import PriceList from "@/components/PriceList.vue";
import FeedbackList from "@/components/FeedbackList.vue";
import FormContactUs from "@/components/FormContactUs.vue";
import TheFooterItem from "@/components/TheFooterItem.vue";
// import SimpleSlider from "@/components/SimpleSlider.vue";
// import CoruselList from "@/components/CoruselList.vue";
let descriptions = {
  header: [
    { title: "Features", href: "#features" },
    { title: "About cats", href: "#about" },
    { title: "Pricing", href: "#pricing" },
    { title: "Reviews", href: "#reviews" },
    { title: "Contacts", href: "#contacts" },
  ],
  mainPage: {
    subtitle: {
      text: "This is a modern cat-cafe",
      style: {
        color: "#fff",
        fontSize: 36,
        fontFamily: "Raleway",
      },
    },
    paragraph: {
      text: "We took the best traditions of the anti-cafe as a basis, added cute kittens and seasoned it all with a cozy atmosphere",
      style: {
        color: "#fff",
        size: 16,
        fontFamily: "Raleway",
      },
    },
    transparentButton: {
      buttonText: "Try",
    },
    formData: {
      inputsplacehoder: [
        { placeholder: "Name" },
        { placeholder: "Email" },
        { placeholder: "Phone" },
      ],
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
      text: "You can find us on social networks",
      style: {
        fontSize: 14,
        fontFamily: "Open Sans",
      },
    },
  },
  aboutPage: {
    tabs: [{ text: "Tab 1" }, { text: "Tab 2" }, { text: "Tab 3" }],
    descriptions: [
      {
        isActive: true,
        subtitle: {
          text: "Tabs 1 with soft transitioning effect",
          style: {
            color: "#333333",
            fontSize: 20,
            fontFamily: "Open Sans",
          },
        },
        paragraph: {
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes.",
          style: {
            fontSize: 14,
            fontFamily: "Open Sans",
          },
        },
      },
      {
        isActive: false,
        subtitle: {
          text: "Tabs 2 with soft transitioning effect",
          style: {
            color: "#333333",
            fontSize: 20,
            fontFamily: "Open Sans",
          },
        },
        paragraph: {
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes.",
          style: {
            fontSize: 14,
            fontFamily: "Open Sans",
          },
        },
      },
      {
        isActive: false,
        subtitle: {
          text: "Tabs 3 with soft transitioning effect",
          style: {
            color: "#333333",
            fontSize: 20,
            fontFamily: "Open Sans",
          },
        },
        paragraph: {
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo. Proin sodales pulvinar tempor. Cum sociis natoque penatibus et magnis dis parturient montes.",
          style: {
            fontSize: 14,
            fontFamily: "Open Sans",
          },
        },
      },
    ],
    imgSrc: "src/assets/img/city.png",
  },
  firstTopicPage: {
    descriptions: {
      subtitle: {
        text: "We offer",
        style: {
          color: "#333333",
          fontSize: 20,
          fontFamily: "Open Sans",
        },
      },
      paragraph: {
        text: "The cost of visiting our anti-cafe includes a lot of buns",
        style: {
          fontSize: 14,
          fontFamily: "Open Sans",
        },
      },
    },
    subList: [
      {
        subTitle: "Cats",
        text: "The cafe is home to 10 cats, which you can pet",
      },
      {
        subTitle: "Tea",
        text: "The cafe has 15 varieties of tea. Try them all!",
      },
      {
        subTitle: "Wi-Fi",
        text: "If you want to work in our cafe, don't worry, we will provide you with access to our high-speed Internet",
      },
    ],
  },
  secondTopicPage: {
    descriptions: {
      subtitle: {
        text: "Cozy place",
        style: {
          color: "#333333",
          fontSize: 20,
          fontFamily: "Open Sans",
        },
      },
      paragraph: {
        text: "In cat-cafe you can have a wonderful time with children, friends. Here you can find 10 board games",
        style: {
          fontSize: 14,
          fontFamily: "Open Sans",
        },
      },
    },
  },
  thirdTopicPage: {
    headerCenter: {
      subtitle: "Why this is awesom",
      paragraph: "We take pets to our cafe from the shelter.",
    },
    reasonItem: [
      {
        imgSrc: "/src/assets/img/icon/done-icon.svg",
        subtitle: "Food",
        paragraph:
          "We feed the cats twice a day. Therefore, it is impossible to feed cats to visitors. You can bring the food with you and leave",
      },
      {
        imgSrc: "/src/assets/img/icon/lapa-icon.svg",
        subtitle: "Cats",
        paragraph:
          "We take new cats from the shelter every month so they can take a break from people's attention",
      },
      {
        imgSrc: "/src/assets/img/icon/like-icon.svg",
        subtitle: "Сare",
        paragraph:
          "If you like some kitty, you can take her to your home and surround her with care and love",
      },
    ],
  },
  pricePage: {
    headerCenter: {
      subtitle: "Pricing",
      paragraph: "You can choose one of the tariffs",
    },
    prices: [
      {
        title: "Hourly",
        cost: "2",
        subtitle: "Free for Life",
        // features: [
        //   "",
        //   "",
        // ],
      },
      {
        title: "All day",
        cost: "10",
        subtitle: "Per hour",
        specialSubtitle: "Our most popular",
        // features: [
        //   "",
        //   "",
        // ],
      },
      {
        title: "For a month",
        cost: "150",
        subtitle: "Monthly Payment",
        // features: [
        //   "",
        //   "",
        // ],
      },
    ],
  },
  feedbackPage: {
    headerCenter: {
      subtitle: "what our customers are saying",
      paragraph:
        "We listen to the feedback of our visitors and strive to make the cafe even better",
    },
    feedbacks: [
      {
        comment:
          "I've known this place for a long time. I often come with friends to play board games. My girlfriend loves the cute kittens that live here",
        name: "Jeremy H.",
        career: "Manager",
        avatarSrc: "/src/assets/img/feedback-people-img/man-1.jpg",
      },
      {
        comment:
          "We come here with the whole family on weekends to take a break from the hustle and bustle of home and spend time with the children",
        name: "Susan W.",
        career: "Photographer",
        avatarSrc: "/src/assets/img/feedback-people-img/woman-1.jpg",
      },
      {
        comment:
          "I work as a freelancer. I like to come here to work, because it's quiet and good music here",
        name: "John S.",
        career: "Freelancer",
        avatarSrc: "/src/assets/img/feedback-people-img/man-2.jpg",
      },
    ],
  },
  fourthTopicPage: {
    headerCenter: {
      subtitle: "Cafe design",
      paragraph:
        "A novice designer took part in creating the style and atmosphere of the cafe",
    },
    transparentButton: {
      buttonText: "Download",
    },
  },
  contactPage: {
    headerCenter: {
      subtitle: "Contact us",
      paragraph:
        "Send us a request to visit the koto cafe. We will definitely call you back to clarify the details of booking a place",
    },
    formData: {
      inputsplacehoder: [
        { placeholder: "Name" },
        { placeholder: "Email" },
        { placeholder: "Phone" },
      ],
    },
  },
  test: {
    slide: [
      "/src/assets/img/banner-main.jpg",
      "/src/assets/img/banner-main.jpg",
      "/src/assets/img/banner-main.jpg",
    ],
  },
};
</script>

<template>
  <TheHeader :headerData="descriptions.header" />
  <main>
    <section class="main-page">
      <div class="container">
        <div class="main-page__description">
          <Logo />
          <DescriptionItem
            :subtitle="descriptions.mainPage.subtitle"
            :paragraph="descriptions.mainPage.paragraph"
          />
          <!-- <TransparentButton
            :buttonText="descriptions.mainPage.transparentButton.buttonText"
          /> -->
        </div>
        <FormMainPage :formData="descriptions.mainPage.formData" />
      </div>
    </section>
    <section class="social-media-page">
      <div class="container">
        <div class="social-media-page__description">
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
    <!-- <section class="about-page">
      <div
        class="container"
        :style="{ backgroundImage: `url(${descriptions.aboutPage.imgSrc})` }"
      >
        <TabsList
          :tabs="descriptions.aboutPage.tabs"
          :descriptions="descriptions.aboutPage.descriptions"
        />
      </div>
    </section> -->
    <section class="first-topic-page" id="features">
      <div class="container">
        <ImgWithShadow
          imgSrc="/src/assets/img/content-cats-img/orange-cat.jpg"
        />
        <div class="first-topic-page__description">
          <DescriptionItem
            :subtitle="descriptions.firstTopicPage.descriptions.subtitle"
            :paragraph="descriptions.firstTopicPage.descriptions.paragraph"
          />
          <SubInfoList :subList="descriptions.firstTopicPage.subList" />
        </div>
      </div>
    </section>
    <section class="second-topic-page">
      <div class="container">
        <div class="second-topic-page__description">
          <DescriptionItem
            :subtitle="descriptions.secondTopicPage.descriptions.subtitle"
            :paragraph="descriptions.secondTopicPage.descriptions.paragraph"
          />
        </div>
        <ImgWithShadow
          imgSrc="/src/assets/img/content-cats-img/brown-cat.jpg"
        />
      </div>
    </section>
    <section class="third-topic-page" id="about">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.thirdTopicPage.headerCenter"
        />
        <ReasonList :itemList="descriptions.thirdTopicPage.reasonItem" />
      </div>
    </section>
    <section class="price-page" id="pricing">
      <div class="container">
        <HeaderCenterPage :description="descriptions.pricePage.headerCenter" />
        <PriceList :prices="descriptions.pricePage.prices" />
      </div>
    </section>
    <section class="feedback-page" id="reviews">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.feedbackPage.headerCenter"
        />
        <!-- <a href="https://ru.freepik.com/free-photo/_10631827.htm#query=man&position=1&from_view=search&track=sph">Изображение от nakaridore</a> на Freepik -->
        <!-- <a href="https://ru.freepik.com/free-photo/_13580471.htm#query=man&position=16&from_view=search&track=sph">Изображение от wayhomestudio</a> на Freepik -->
        <!-- <a href="https://ru.freepik.com/free-photo/_9631091.htm#query=woman&position=13&from_view=search&track=sph">Изображение от marymarkevich</a> на Freepik -->
        <FeedbackList :feedbacks="descriptions.feedbackPage.feedbacks" />
      </div>
    </section>
    <section class="fourth-topic-page">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.fourthTopicPage.headerCenter"
          :class="{ colorWhite: true }"
        />
        <!-- <TransparentButton
          :buttonText="
            descriptions.fourthTopicPage.transparentButton.buttonText
          "
        /> -->
      </div>
    </section>
    <section class="contact-page" id="contacts">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.contactPage.headerCenter"
        />
        <FormContactUs :formData="descriptions.contactPage.formData" />
      </div>
    </section>
    <section class="footer-page">
      <TheFooterItem />
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
@media (max-width: 769px) {
  .main-page {
    height: 100%;
  }
}
@media (max-width: 769px) {
  .main-page .container {
    flex-direction: column;
    align-items: center;
  }
}
.main-page__description {
  width: 60%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-right: 9em;
}
@media (max-width: 769px) {
  .main-page__description {
    width: 100%;
    margin: 0 0 2em 0;
  }
}
.main-page .transparent-btn {
  margin-top: 3em;
}
.social-media-page {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f5f5f5;
  /* height: 10vh; */
}
.social-media-page .container {
  padding: 1em 0;
}
@media (max-width: 600px) {
  .social-media-page .container {
    flex-direction: column;
    align-items: center;
  }
}
.social-media-page__description {
  width: 40%;
}
@media (max-width: 769px) {
  .social-media-page__description {
    width: 50%;
  }
}
@media (max-width: 600px) {
  .social-media-page__description {
    width: 100%;
    margin-bottom: 1em;
    text-align: center;
  }
}
.about-page {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f5f5f5;
}
.about-page .container {
  justify-content: space-between;
  background-repeat: no-repeat;
  background-position: right center;
}
@media (max-width: 769px) {
  .about-page .container {
    background: none !important;
  }
}
.first-topic-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
@media (max-width: 769px) {
  .first-topic-page .container {
    flex-direction: column;
    align-items: center;
  }
}
.first-topic-page__description {
  width: 55%;
  margin-left: 10em;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
@media (max-width: 769px) {
  .first-topic-page__description {
    width: 100%;
    margin: 3em 0 0;
  }
}
.second-topic-page {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f5f5f5;
}

.second-topic-page .container {
  justify-content: space-between;
}
@media (max-width: 769px) {
  .second-topic-page .container {
    flex-direction: column;
    align-items: center;
  }
}
.second-topic-page__description {
  width: 43%;
}
@media (max-width: 769px) {
  .second-topic-page__description {
    width: 100%;
    margin: 0 0 3em;
  }
}
.section-topic--page .img-with-shadow {
  width: 40%;
}
.third-topic-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
.third-topic-page .container {
  flex-direction: column;
  align-items: center;
}
.price-page {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f5f5f5;
}
.price-page .container {
  flex-direction: column;
  align-items: center;
}
.price-list {
  margin-top: 4em;
}
.feedback-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
.feedback-page .container {
  flex-direction: column;
  align-items: center;
}
/* .feedback-list {
  margin-top: 4em;
} */
.fourth-topic-page {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  /* height: 55vh; */
  background: #7c7c7c url(@/assets/img/banner-main.jpg) no-repeat center/cover;
  background-blend-mode: multiply;
}
.fourth-topic-page .container {
  flex-direction: column;
  align-items: center;
  padding: 3em 0;
}
.contact-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
.contact-page .container {
  flex-direction: column;
  align-items: center;
}
</style>
