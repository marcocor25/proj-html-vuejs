<template>
  <div id="app">
    <TopBanner />
    <MyHeader />
    <MyNav />
    <CardSection />
    <PostSection />
    <MidBanner />
  </div>
</template>

<script>
import TopBanner from "./components/TopBanner.vue";
import MyHeader from "./components/MyHeader.vue";
import MyNav from "./components/MyNav.vue";
import CardSection from "./components/CardSection.vue";
import PostSection from "./components/PostSection.vue";
import MidBanner from "./components/MidBanner.vue";

export default {
  name: "App",
  components: {
    TopBanner,
    MyHeader,
    MyNav,
    CardSection,
    PostSection,
    MidBanner,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/colors.scss";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img {
  display: block;
  width: 100%;
  height: 100%;
  user-select: none;
  -webkit-user-drag: none;
}

ul {
  list-style: none;
}

#app {
  height: 6000px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 14px;
  color: $default-black;
}
</style>
