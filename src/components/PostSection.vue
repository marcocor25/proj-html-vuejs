<template>
  <div class="container-fluid">
    <div class="container">
      <MyPosts />
    </div>
  </div>
</template>

<script>
import MyPosts from "./MyPosts.vue";

export default {
  name: "PostSection",
  components: {
    MyPosts,
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
  }
}
</style>
