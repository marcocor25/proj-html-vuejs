<template>
  <div class="col-2">
    <div class="twitter">
      <h3>latest from twitter</h3>
    </div>
    <div class="instagram">
      <h3>photos from instagram</h3>
      <div class="small-images">
        <figure v-for="el in smallImages" :key="el.id">
          <img :src="el.imgUrl" :alt="el.id" />
        </figure>
      </div>
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
      smallImages: [
        {
          id: 1,
          imgUrl: require(`../assets/img/29739607_2020680068220520_4509928046932787200_n.jpg`),
        },
        {
          id: 2,
          imgUrl: require(`../assets/img/30087804_253872848488989_8792603541668626432_n.jpg`),
        },
        {
          id: 3,
          imgUrl: require(`../assets/img/29415620_196477127626244_3250318472361541632_n.jpg`),
        },
        {
          id: 4,
          imgUrl: require(`../assets/img/30078414_1274410412703843_8290935809419247616_n.jpg`),
        },
        {
          id: 5,
          imgUrl: require(`../assets/img/30077195_2066750973610181_3733150062893596672_n.jpg`),
        },
        {
          id: 6,
          imgUrl: require(`../assets/img/29415304_166583630713703_1032667922171953152_n.jpg`),
        },
      ],
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
    padding-bottom: 12px;
    text-transform: uppercase;
    font-weight: bolder;
    color: $dark;
  }

  .instagram {
    min-height: 230px;

    .small-images {
      display: flex;
      flex-wrap: wrap;
      cursor: pointer;
      transition: 200ms linear;

      &:hover {
        filter: brightness(0.8);
      }

      figure {
        width: calc(100% / 3);
        aspect-ratio: 1;
      }
    }
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
          transform: scale(1.05);
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
