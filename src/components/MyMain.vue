<template>
  <div class="container">
    <CardsSection />
  </div>
</template>

<script>
import CardsSection from "./CardsSections.vue";

export default {
  name: "MyNav",
  components: {
    CardsSection,
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

.container {
  @include container;
}
</style>
