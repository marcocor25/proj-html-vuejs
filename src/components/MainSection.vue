<template>
  <div class="container-fluid">
    <div class="container">
      <MainColLarge />
      <MainColSmall />
    </div>
  </div>
</template>

<script>
import MainColLarge from "./MainColLarge.vue";
import MainColSmall from "./MainColSmall.vue";

export default {
  name: "MainSection",
  components: {
    MainColLarge,
    MainColSmall,
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
  background: $default;

  .container {
    @include container;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }
}
</style>
