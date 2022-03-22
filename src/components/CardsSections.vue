<template>
  <section class="cards">
    <div v-for="el in cards" :key="el.id" class="card">
      <figure>
        <img :src="el.imgUrl" :alt="el.title" />
      </figure>
      <div class="overlay">
        <div class="badge">
          {{ el.title }}
        </div>
        <h3>{{ el.text }}</h3>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CardsSection",
  data() {
    return {
      cards: [
        {
          id: 1,
          title: "photography",
          text: "how to take better concert pictures in 30 seconds",
          imgUrl: require(`../assets/img/blog-46.jpg`),
        },
        {
          id: 2,
          title: "gadgets",
          text: "gadgets that make your smartphone even smarter",
          imgUrl: require(`../assets/img/blog-47.jpg`),
        },
        {
          id: 3,
          title: "travel",
          text: "20 top-rated tourist attractions in manhattan",
          imgUrl: require(`../assets/img/blog-48.jpg`),
        },
        {
          id: 4,
          title: "lifestyle",
          text: "the best way to ride a motorcycle",
          imgUrl: require(`../assets/img/blog-49.jpg`),
        },
        {
          id: 5,
          title: "travel",
          text: "5 fun things to do at the beach",
          imgUrl: require(`../assets/img/blog-50.jpg`),
        },
        {
          id: 6,
          title: "recipes",
          text: "amazingly fresh fruit and herb drinks for summer",
          imgUrl: require(`../assets/img/blog-51.jpg`),
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

.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 25px;
  padding: 40px 0;
  background: skyblue;

  .card {
    flex-grow: 1;
    width: calc((100% / 3) - 25px);
    min-height: 200px;
    cursor: pointer;
    transition: 200ms linear;
    position: relative;

    &:hover {
      transform: scale(0.97);
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      padding: 18px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-items: flex-start;
      gap: 5px;
      background: rgba($color: #000000, $alpha: 0.3);

      h3 {
        font-size: 18px;
        font-weight: bolder;
        text-transform: capitalize;
        color: $default;
      }

      .badge {
        padding: 5px;
        text-transform: uppercase;
        font-weight: bolder;
        font-size: 8px;
        color: $default;
        background: $top-banner;
      }
    }
  }
}
</style>
