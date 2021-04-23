<template>
  <div id="section_4">
    <a href="#" className="w100">
      <img :src="feat_img" className="w100" />
    </a>
  </div>
</template>

<script>
export default {
  name: "SectionOneCol",
  props: {
    feat_img: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>