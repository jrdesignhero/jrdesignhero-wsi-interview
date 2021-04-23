<template>
  <div>
    <Hero :img="hero.img"></Hero>

    <SectionTwoCol
      :img_1="sectionOne.img_1"
      :img_2="sectionOne.img_2"
    ></SectionTwoCol>

    <SectionFeatFiveCol
      :feat_img="sectionTwo.feat_img"
      :img_1="sectionTwo.img_1"
      :img_2="sectionTwo.img_2"
      :img_3="sectionTwo.img_3"
      :img_4="sectionTwo.img_4"
      :img_5="sectionTwo.img_5"
    ></SectionFeatFiveCol>

    <SectionOneCol :feat_img="sectionThree.feat_img"></SectionOneCol>

    <SectionOneCol :feat_img="sectionFour.feat_img"></SectionOneCol>

    <SectionOneCol :feat_img="sectionFive.feat_img"></SectionOneCol>

    <SectionFeatFiveCol
      :feat_img="sectionSix.feat_img"
      :img_1="sectionSix.img_1"
      :img_2="sectionSix.img_2"
      :img_3="sectionSix.img_3"
      :img_4="sectionSix.img_4"
      :img_5="sectionSix.img_5"
    ></SectionFeatFiveCol>

    <SectionOneCol :feat_img="sectionSeven.feat_img"></SectionOneCol>

    <SectionOneCol :feat_img="sectionEight.feat_img"></SectionOneCol>

    <SectionOneCol :feat_img="sectionNine.feat_img"></SectionOneCol>

    <SectionOneCol :feat_img="sectionTen.feat_img"></SectionOneCol>

    <SectionTwoCol
      :img_1="sectionEleven.img_1"
      :img_2="sectionEleven.img_2"
    ></SectionTwoCol>

    <SectionOneCol :feat_img="sectionTwelve.feat_img"></SectionOneCol>
    <SectionOneCol :feat_img="sectionThirteen.feat_img"></SectionOneCol>
    <SectionOneCol :feat_img="sectionFourteen.feat_img"></SectionOneCol>

    <SectionTwoCol
      :img_1="sectionFifteen.img_1"
      :img_2="sectionFifteen.img_2"
    ></SectionTwoCol>

    <SectionOneCol :feat_img="sectionSixteen.feat_img"></SectionOneCol>

    <SectionThreeCol
      :img_1="sectionSeventeen.img_1"
      :img_2="sectionSeventeen.img_2"
      :img_3="sectionSeventeen.img_3"
    ></SectionThreeCol>

    <SectionThreeCol
      :img_1="sectionEighteen.img_1"
      :img_2="sectionEighteen.img_2"
      :img_3="sectionEighteen.img_3"
    ></SectionThreeCol>

    <SectionThreeCol
      :img_1="sectionNineteen.img_1"
      :img_2="sectionNineteen.img_2"
      :img_3="sectionNineteen.img_3"
    ></SectionThreeCol>
  </div>
</template>

<script>
import Hero from "./layouts/Hero.vue";
import SectionTwoCol from "./layouts/SectionTwoCol.vue";
import SectionThreeCol from "./layouts/SectionThreeCol.vue";
import SectionFeatFiveCol from "./layouts/SectionFeatFiveCol.vue";
import SectionOneCol from "./layouts/SectionOneCol.vue";

export default {
  data: () => {
    return {
      hero: {
        img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/023.jpg",
      },
      sectionOne: {
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/025.jpg",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/022.jpg",
      },
      sectionTwo: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/026.jpg",
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202115/1608/001/004.jpg",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/008.jpg",
        img_3:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/006.jpg",
        img_4:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/003.jpg",
        img_5:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/010.jpg",
      },
      sectionThree: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/019.jpg",
      },
      sectionFour: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202116/0258/001/003.jpg",
      },
      sectionFive: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/i/202116/0001/images/ecm-content/ws-design-chat-banner-hp.jpg",
      },
      sectionSix: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202115/1284/001/001.jpg",
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/005.jpg",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1542/001/001.jpg",
        img_3:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/001.jpg",
        img_4:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/007.jpg",
        img_5:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/1049/001/004.jpg",
      },
      sectionSeven: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202117/0720/001/001.jpg",
      },
      sectionEight: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202052/3185/001/001.gif",
      },
      sectionNine: {
        feat_img:
          "https://www.williams-sonoma.com/netstorage/images/CatAffinity-spr121-Cutlery.jpg",
      },
      sectionTen: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202111/1545/001/001.jpg",
      },
      sectionEleven: {
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202109/0958/001/009.jpg",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202109/0958/001/004.jpg",
      },
      sectionTwelve: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202113/2223/001/001.jpg",
      },
      sectionThirteen: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202109/0958/001/010.jpg",
      },
      sectionFourteen: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202111/0325/001/001.jpg",
      },
      sectionFifteen: {
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202109/0958/001/001.jpg",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202109/0958/001/002.jpg",
      },
      sectionSixteen: {
        feat_img:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202052/1964/001/001.jpg",
      },
      sectionSeventeen: {
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202115/1608/001/003.jpg",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202116/0443/001/001.jpg",
        img_3:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202115/1608/001/002.jpg",
      },
      sectionEighteen: {
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202041/2579/053/010.jpg",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202041/2579/053/546.jpg",
        img_3:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202041/2579/051/611.jpg",
      },
      sectionNineteen: {
        img_1:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202111/1539/001/003.gif",
        img_2:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202111/1539/001/001.gif",
        img_3:
          "https://assets.wsimgs.com/wsimgs/rk/images/dp/ecm/202111/1539/001/002.gif",
      },
    };
  },

  name: "Template",
  components: {
    Hero,
    SectionTwoCol,
    SectionThreeCol,
    SectionFeatFiveCol,
    SectionOneCol,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.reset {
  position: relative;
  overflow: hidden;
}
.w33 {
  width: 33.3%;
  display: block;
}
.w20 {
  width: 20%;
  display: block;
}
.w50 {
  width: 50%;
  display: block;
}
.w100 {
  display: block;
  width: 100%;
}
.f-left {
  float: left;
}
.f-right {
  float: right;
}
</style>
