<template>
  <section class="posts">
    <div class="col-10">
      <h1>Test</h1>
    </div>
    <div class="col-2">
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
  padding: 40px 0;

  .col-10 {
    flex-grow: 0.7;
    border: 2px dashed blue;
  }

  .col-2 {
    flex-grow: 0.3;
    border: 2px dashed orange;
  }
}
</style>
