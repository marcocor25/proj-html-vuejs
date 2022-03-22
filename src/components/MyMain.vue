<template>
  <div class="container-fluid">
    <div class="container">
      <CardsSection />
      <PostSection />
    </div>
  </div>
</template>

<script>
import CardsSection from "./CardsSections.vue";
import PostSection from "./PostSection.vue";

export default {
  name: "MyNav",
  components: {
    CardsSection,
    PostSection,
  },
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
  background: $smoke;
  height: 530px;

  .container {
    @include container;
  }
}
</style>
