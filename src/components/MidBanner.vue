<template>
  <div class="mid-banner">
    <div class="container">
      <h1>Ciao</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "MidBanner",
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";
@import "../assets/scss/mixins.scss";

.mid-banner {
  background: $cobalto;

  .container {
    @include container;
    min-height: 150px;
    display: flex;
    align-items: center;
    color: $default;
  }
}
</style>
