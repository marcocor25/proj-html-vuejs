<template>
  <div class="col-2">
    <div class="twitter">
      <h3>latest from twitter</h3>
    </div>
    <div class="instagram">
      <h3>photos from instagram</h3>
    </div>
    <div class="tags">
      <h3>tags</h3>
      <div class="tag-wrapper">
        <div v-for="el in tags" :key="el.id" class="tag">
          {{ el.text }}
        </div>
      </div>
    </div>
    <div class="find-us">
      <h3>find us on facebook</h3>
      <div class="text">okler themes</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainColSmall",
  data() {
    return {
      tags: [
        {
          id: 1,
          text: "design",
        },
        {
          id: 2,
          text: "brands",
        },
        {
          id: 3,
          text: "video",
        },
        {
          id: 4,
          text: "business",
        },
        {
          id: 5,
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

.col-2 {
  width: 23%;
  padding: 40px 0;
  display: flex;
  flex-direction: column;
  gap: 20px;

  h3 {
    padding-bottom: 10px;
    text-transform: uppercase;
    color: $dark;
  }

  .twitter,
  .instagram {
    min-height: 220px;
    background: yellow;
  }

  .tags {
    min-height: 100px;

    .tag-wrapper {
      display: flex;
      flex-wrap: wrap;
      gap: 5px;

      .tag {
        padding: 3px 5px;
        border-radius: 20px;
        text-transform: uppercase;
        font-weight: bolder;
        font-size: 9px;
        cursor: pointer;
        color: $smoke;
        background: $dark-bkg;
        transition: 200ms linear;

        &:hover {
          transform: scale(1.1);
        }
      }
    }
  }

  .find-us {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    .text {
      padding: 10px;
      border-left: 3px solid $light-border;
      text-transform: capitalize;
      font-weight: 500;
      cursor: pointer;
      color: $cobalto;

      &:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>
