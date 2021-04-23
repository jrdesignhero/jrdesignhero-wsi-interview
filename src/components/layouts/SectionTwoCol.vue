<template>
  <div id="feature_2" className="reset">
    <div className="f-left w50">
      <img className="w100" :src="img_1" />
    </div>
    <div className="f-right w50">
      <img className="w100" :src="img_2" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionTwoCol",
  props: {
    img_1: String,
    img_2: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>