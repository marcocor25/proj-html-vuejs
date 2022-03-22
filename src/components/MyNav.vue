<template>
  <nav>
    <ul class="nav-links">
      <div class="li-wrapper">
        <li
          v-for="el in links"
          :key="el.id"
          :class="el.active == true ? 'active' : ''"
        >
          {{ el.text }}
        </li>
      </div>
      <i class="fa-solid fa-magnifying-glass"></i>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "MyNav",
  data() {
    return {
      links: [
        {
          id: 1,
          text: "home",
          active: true,
        },
        {
          id: 2,
          text: "elements",
          active: false,
        },
        {
          id: 3,
          text: "features",
          active: false,
        },
        {
          id: 4,
          text: "pages",
          active: false,
        },
        {
          id: 5,
          text: "portfolio",
          active: false,
        },
        {
          id: 6,
          text: "blog",
          active: false,
        },
        {
          id: 7,
          text: "shop",
          active: false,
          space: true,
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/colors.scss";
@import "../assets/scss/mixins.scss";

nav {
  background: $default;

  .nav-links {
    @include container;
    min-height: 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-weight: bolder;
    text-transform: uppercase;
    color: $dark;

    i {
      cursor: pointer;
    }

    .li-wrapper {
      display: flex;
      align-items: center;
      gap: 20px;

      li {
        cursor: pointer;
        &:hover {
          text-decoration: underline;
        }
      }

      .active {
        color: $top-banner;
      }
    }
  }
}
</style>
