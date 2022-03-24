<template>
  <div class="container-fluid">
    <div class="container">
      <div class="badge-wrapper">
        <div class="triangle"></div>
        <div class="badge">Get in Touch</div>
      </div>
      <div class="col large"></div>
      <div class="col"></div>
      <div class="col"></div>
      <div class="col"></div>
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
    display: flex;
    padding: 60px 0;
    position: relative;

    .badge-wrapper {
      display: flex;
      cursor: default;
      position: absolute;
      top: -13px;

      .triangle {
        width: 0;
        height: 0;
        border-style: solid;
        border-width: 0 0 13px 10px;
        border-color: transparent transparent #005580 transparent;
      }

      .badge {
        padding: 5px 15px;
        font-family: "Shadows Into Light", cursive;
        font-size: 18px;
        user-select: none;
        color: $smoke;
        background: $cobalto;
      }
    }

    .col {
      width: 23%;
      min-height: 230px;
      border: 2px dashed yellow;
    }

    .large {
      flex-grow: 1;
    }
  }
}
</style>
