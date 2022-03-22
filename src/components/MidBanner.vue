<template>
  <div class="mid-banner">
    <div class="container">
      <div class="round">
        <i class="fa-solid fa-chevron-left"></i>
      </div>
      <div class="button-wrapper">
        <div v-for="el in buttons" :key="el.id" class="button">
          <h3>
            {{ el.text }}
          </h3>
        </div>
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
    return {
      buttons: [
        {
          id: 1,
          text: "gadgets",
        },
        {
          id: 2,
          text: "photography",
        },
        {
          id: 3,
          text: "lifestyle",
        },
        {
          id: 4,
          text: "fashion",
        },
        {
          id: 5,
          text: "recipes",
        },
        {
          id: 6,
          text: "travel",
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

.mid-banner {
  background: $cobalto;

  .container {
    @include container;
    min-height: 150px;
    display: flex;
    align-items: center;

    .button-wrapper {
      flex-grow: 1;
      display: flex;
      justify-content: space-evenly;

      .button {
        width: calc((100% / 6) - 25px);
        min-height: 45px;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        color: $default;
        transition: 200ms linear;
        background: $dark-bkg;

        h3 {
          text-transform: uppercase;
        }

        &:hover {
          transform: scale(0.96);
          background: $button-hover;
        }
      }
    }

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
