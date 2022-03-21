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

.top-banner {
  background: $top-banner;

  .container {
    width: 1200px;
    min-height: 50px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    gap: 20px;
    color: $default;
    border: 2px dashed red;

    h5 {
      cursor: default;
    }

    .banner-links {
      display: flex;
      gap: 20px;
      cursor: pointer;
      font-weight: bolder;
      text-transform: uppercase;

      li:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>
