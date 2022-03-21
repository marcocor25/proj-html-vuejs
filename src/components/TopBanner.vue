<template>
  <div class="top-banner">
    <div class="container">
      <h3>Test colori</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopBanner",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";

.top-banner {
  background: $top-banner;

  .container {
    width: 1000px;
    min-height: 40px;
    margin: 0 auto;
    color: $default;
    border: 2px dashed red;
  }
}
</style>
