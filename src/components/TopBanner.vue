<template>
  <div class="top-banner">
    <div class="container">
      <h5>Everything about Lifestyle, Travel and Gadgets!</h5>
      <ul class="banner-links">
        <li v-for="(el, i) in links" :key="i">
          {{ el }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopBanner",
  data() {
    return {
      links: ["sign in", "about us", "contact us", "buy now"],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";
@import "../assets/scss/mixins.scss";

.top-banner {
  position: sticky;
  top: 0;
  left: 0;
  z-index: 999;
  background: $top-banner;

  .container {
    @include container;
    min-height: 50px;
    display: flex;
    align-items: center;
    gap: 20px;
    color: $default;

    h5 {
      cursor: default;
    }

    .banner-links {
      display: flex;
      gap: 20px;
      font-weight: bolder;
      text-transform: uppercase;

      li {
        cursor: pointer;
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
}
</style>
