<template>
  <div id="section_3">
    <div className="sectionHero">
      <img :src="feat_img" className="w100" />
    </div>

    <div className="sectionSubFeature">
      <a href="#" className="w20 f-left">
        <img :src="img_1" className="w100" />
      </a>
      <a href="#" className="w20 f-left">
        <img :src="img_2" className="w100" />
      </a>
      <a href="#" className="w20 f-left">
        <img :src="img_3" className="w100" />
      </a>
      <a href="#" className="w20 f-left">
        <img :src="img_4" className="w100" />
      </a>
      <a href="#" className="w20 f-left">
        <img :src="img_5" className="w100" />
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionFeatFiveCol",
  props: {
    feat_img: String,
    img_1: String,
    img_2: String,
    img_3: String,
    img_4: String,
    img_5: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>