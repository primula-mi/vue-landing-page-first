<script setup>
import TheHeader from "@/components/TheHeader.vue";
import Logo from "@/components/LogoItem.vue";
import DescriptionItem from "@/components/DescriptionItem.vue";
import TransparentButton from "@/components/TransparentButton.vue";
import FormMainPage from "@/components/FormMainPage.vue";
import SubtitleItem from "@/components/SubtitleItem.vue";
import ParagraphItem from "@/components/ParagraphItem.vue";
import SocialMedia from "@/components/SocialMedia.vue";
import TabsList from "@/components/TabsList.vue";
import ImgWithShadow from "@/components/ImgWithShadow.vue";
import SubListWithIcon from "@/components/SubListWithIcon.vue";
import HeaderCenterPage from "@/components/HeaderCenterPage.vue";
import ReasonList from "@/components/ReasonList.vue";
import PriceList from "@/components/PriceList.vue";
import FeedbackList from "@/components/FeedbackList.vue";
import FormContactUs from "@/components/FormContactUs.vue";
import FooterItem from "@/components/FooterItem.vue";
let descriptions = {
  header: [
    { title: "Features", href: "#features" },
    { title: "About", href: "#about" },
    { title: "Pricing", href: "#pricing" },
    { title: "Reviews", href: "#reviews" },
    { title: "Contacts", href: "#contacts" },
  ],
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
  aboutPage: {
    tabs: [
      { text: "Tab 1", isActive: true },
      { text: "Tab 2", isActive: false },
      { text: "Tab 3", isActive: false },
    ],
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
  },
  firstTopicPage: {
    descriptions: {
      subtitle: {
        text: "Sub list section",
        style: {
          color: "#333333",
          fontSize: 20,
          fontFamily: "Open Sans",
        },
      },
      paragraph: {
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra justo commodo.",
        style: {
          fontSize: 14,
          fontFamily: "Open Sans",
        },
      },
    },
    subList: [
      {
        subTitle: "Title",
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
      },
      {
        subTitle: "Title",
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet.",
      },
    ],
  },
  secondTopicPage: {
    descriptions: {
      subtitle: {
        text: "Standart pictures section",
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
  },
  thirdTopicPage: {
    headerCenter: {
      subtitle: "Why this is awesom",
      paragraph: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    },
    reasonItem: [
      {
        imgSrc: "/src/assets/img/icon/done-icon.svg",
        subtitle: "Thoughtful Design",
        paragraph:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra",
      },
      {
        imgSrc: "/src/assets/img/icon/lapa-icon.svg",
        subtitle: "Well Crafted",
        paragraph:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra",
      },
      {
        imgSrc: "/src/assets/img/icon/like-icon.svg",
        subtitle: "Easy to Customize",
        paragraph:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean euismod bibendum laoreet. Proin gravida dolor sit amet lacus accumsan et viverra",
      },
    ],
  },
  pricePage: {
    headerCenter: {
      subtitle: "Pricing option",
      paragraph: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    },
    prices: [
      {
        title: "Basic",
        cost: "0",
        subtitle: "Free for Life",
        features: [
          "1 gb of space",
          "10 gb of bandwidth",
          "3 websites",
          "Basic Customization",
          "Wordpress integration",
          "Email support",
        ],
      },
      {
        title: "Professional",
        cost: "19",
        subtitle: "Monthly Payment",
        specialSubtitle: "Our most popular",
        features: [
          "5 gb of space",
          "50 gb of bandwidth",
          "12 websites",
          "Advanced Customization",
          "Wordpress integration",
          "Email support",
        ],
      },
      {
        title: "Enterprise",
        cost: "70",
        subtitle: "Monthly Payment",
        features: [
          "Unlimited space",
          "unlimited bandwidth",
          "100 websites",
          "Advanced Customization",
          "Wordpress integration",
          "24/7 customer support",
        ],
      },
    ],
  },
  feedbackPage: {
    headerCenter: {
      subtitle: "what our customers are saying",
      paragraph: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    },
    feedbacks: [
      {
        comment:
          "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloribus accusamus expedita repellat similique odio aspernatur ex, architecto eaque quo suscipit.",
        name: "Jeremy H.",
        career: "Manager",
        avatarSrc: "/src/assets/img/icon/done-icon.svg",
      },
      {
        comment:
          "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloribus accusamus expedita repellat similique odio aspernatur ex, architecto eaque quo suscipit.",
        name: "John S.",
        career: "Freelancer",
        avatarSrc: "/src/assets/img/icon/lapa-icon.svg",
      },
      {
        comment:
          "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloribus accusamus expedita repellat similique odio aspernatur ex, architecto eaque quo suscipit.",
        name: "Susan W.",
        career: "Photographer",
        avatarSrc: "/src/assets/img/icon/like-icon.svg",
      },
    ],
  },
  fourthTopicPage: {
    headerCenter: {
      subtitle: "Stylish axure design",
      paragraph:
        "Use the sections you need, remove the ones you don't.  Create gorgeous prototypes faster than ever!",
    },
    transparentButton: {
      buttonText: "Download",
    },
  },
  contactPage: {
    headerCenter: {
      subtitle: "Contact us",
      paragraph: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    },
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
          <TransparentButton
            :buttonText="descriptions.mainPage.transparentButton.buttonText"
          />
        </div>
        <FormMainPage />
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
    <section class="about-page">
      <div class="container">
        <TabsList
          :tabs="descriptions.aboutPage.tabs"
          :descriptions="descriptions.aboutPage.descriptions"
        />
        <img class="about-page__img" src="@/assets/img/city.png" alt="" />
      </div>
    </section>
    <section class="first-topic-page">
      <div class="container">
        <ImgWithShadow imgSrc="/src/assets/img/banner-main.jpg" />
        <div class="first-topic-page__description">
          <DescriptionItem
            :subtitle="descriptions.firstTopicPage.descriptions.subtitle"
            :paragraph="descriptions.firstTopicPage.descriptions.paragraph"
          />
          <SubListWithIcon :subList="descriptions.firstTopicPage.subList" />
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
        <ImgWithShadow imgSrc="/src/assets/img/banner-main.jpg" />
      </div>
    </section>
    <section class="third-topic-page">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.thirdTopicPage.headerCenter"
        />
        <ReasonList :itemList="descriptions.thirdTopicPage.reasonItem" />
      </div>
    </section>
    <section class="price-page">
      <div class="container">
        <HeaderCenterPage :description="descriptions.pricePage.headerCenter" />
        <PriceList :prices="descriptions.pricePage.prices" />
      </div>
    </section>
    <section class="feedback-page">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.feedbackPage.headerCenter"
        />
        <FeedbackList :feedbacks="descriptions.feedbackPage.feedbacks" />
      </div>
    </section>
    <section class="fourth-topic-page">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.fourthTopicPage.headerCenter"
          :class="{ colorWhite: true }"
        />
        <TransparentButton
          :buttonText="
            descriptions.fourthTopicPage.transparentButton.buttonText
          "
        />
      </div>
    </section>
    <section class="contact-page">
      <div class="container">
        <HeaderCenterPage
          :description="descriptions.contactPage.headerCenter"
        />
        <FormContactUs />
      </div>
    </section>
    <section class="footer-page">
      <FooterItem />
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
.social-media-page {
  display: flex;
  justify-content: center;
  align-items: center;
  /* height: 10vh; */
}
.social-media-page .container {
  padding: 1em 0;
}
.social-media-page__description {
  width: 40%;
  /* margin: 1em 0; */
}
.about-page {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f5f5f5;
}
.about-page__img {
  width: 25%;
}
.first-topic-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
.first-topic-page__description {
  width: 55%;
  margin-left: 10em;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
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
.second-topic-page__description {
  width: 43%;
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
.feedback-list {
  margin-top: 4em;
}
.fourth-topic-page {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 55vh;
  background: #7c7c7c url(@/assets/img/banner-main.jpg) no-repeat center/cover;
  background-blend-mode: multiply;
}
.fourth-topic-page .container {
  flex-direction: column;
  align-items: center;
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
