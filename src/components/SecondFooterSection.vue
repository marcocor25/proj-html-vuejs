<template>
  <div class="container-fluid">
    <div class="container">
      <figure>
        <img src="../assets/img/logo-footer.png" />
      </figure>
      <span>© copyright 2020. all rights reserved.</span>
      <div class="wrapper">
        <div v-for="el in items" :key="el.id" class="item">
          <i class="fa-solid fa-chevron-right"></i>
          <p>
            {{ el.text }}
          </p>
        </div>
      </div>
    </div>
    <a href="#" title="Vai a inizio pagina" class="top-page">
      <i class="fa-solid fa-chevron-up"></i>
    </a>
  </div>
</template>

<script>
export default {
  name: "SecondFooterSection",
  data() {
    return {
      items: [
        {
          id: 1,
          text: "FAQ's",
        },
        {
          id: 2,
          text: "Sitemap",
        },
        {
          id: 3,
          text: "Contact Us",
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

.container-fluid {
  background: $extra-dark;
  position: relative;

  .top-page {
    position: absolute;
    bottom: 0;
    right: 10px;
    padding: 15px;
    border-radius: 5px;
    font-size: 8px;
    color: $smoke;
    background: $mid-grey;
  }

  .container {
    @include container;
    min-height: 80px;
    display: flex;
    align-items: center;
    gap: 20px;
    font-size: 12px;

    figure {
      width: 75px;
      filter: brightness(0.5);
    }

    span {
      flex-grow: 1;
      text-transform: capitalize;
      color: $mid-grey;
    }

    .wrapper {
      display: flex;
      gap: 10px;

      .item {
        display: flex;
        align-items: center;
        gap: 3px;
        font-weight: bolder;
        cursor: pointer;
        color: $mid-grey;

        i {
          font-size: 7px;
        }

        p:hover {
          text-decoration: underline;
          color: $light-grey;
        }
      }
    }
  }
}
</style>
