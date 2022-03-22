<template>
  <div class="container-fluid">
    <div class="container">
      <MyCards />
    </div>
  </div>
</template>

<script>
import MyCards from "./MyCards.vue";

export default {
  name: "CardSection",
  components: {
    MyCards,
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

  .container {
    @include container;
  }
}
</style>
