<template>
  <div class="header">
    <div class="container">
      <figure class="logo">
        <img src="../assets/img/logo-default-slim.png" />
      </figure>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyHeader",
  data() {
    return {};
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";
@import "../assets/scss/mixins.scss";

.header {
  background: $default;
  border-bottom: 1px solid $light-border;

  .container {
    @include container;
    min-height: 100px;
    display: flex;
    align-items: center;

    .logo {
      width: 100px;
    }
  }
}
</style>
