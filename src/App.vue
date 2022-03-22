<template>
  <div id="app">
    <TopBanner />
    <MyHeader />
    <MyNav />
  </div>
</template>

<script>
import TopBanner from "./components/TopBanner.vue";
import MyHeader from "./components/MyHeader.vue";
import MyNav from "./components/MyNav.vue";

export default {
  name: "App",
  components: {
    TopBanner,
    MyHeader,
    MyNav,
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 14px;
  color: #000000;
  background: $body;
}
</style>
