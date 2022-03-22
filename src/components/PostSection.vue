<template>
  <section class="posts">
    <div class="col-4">
      <h1>Test</h1>
    </div>
    <div class="col-4">
      <h1>Test</h1>
    </div>
    <div class="col-4">
      <h1>Test</h1>
    </div>
  </section>
</template>

<script>
export default {
  name: "PostSection",
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";
@import "../assets/scss/mixins.scss";

.posts {
  min-height: 500px;
  display: flex;
  justify-content: space-between;
  padding: 40px 0;

  .col-4 {
    width: calc((100% / 3) - 20px);
    border: 2px dashed blue;
  }
}
</style>
