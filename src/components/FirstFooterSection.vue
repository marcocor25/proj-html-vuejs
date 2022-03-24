<template>
  <div class="container-fluid">
    <div class="container">
      <h1>Ciao</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "FirstFooterSection",
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";
@import "../assets/scss/mixins.scss";

.container-fluid {
  background: $dark-bkg;

  .container {
    @include container;
    min-height: 300px;
  }
}
</style>
