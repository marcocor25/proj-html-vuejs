<template>
  <div class="col-10">
    <h1>ciao</h1>
  </div>
</template>

<script>
export default {
  name: "MainColLarge",
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";
@import "../assets/scss/mixins.scss";

.col-10 {
  width: 68%;
  padding: 40px 0;
}
</style>
