<template>
  <div class="mid-banner">
    <div class="container">
      <div class="round">
        <i class="fa-solid fa-chevron-left"></i>
      </div>

      <div class="round">
        <i class="fa-solid fa-chevron-right"></i>
      </div>
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
    justify-content: space-between;
    align-items: center;
    color: $default;

    .round {
      width: 40px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50%;
      cursor: pointer;
      transition: 200ms linear;
      color: $dark;

      &:hover {
        background: rgba($color: #ffffff, $alpha: 0.5);
      }
    }
  }
}
</style>
