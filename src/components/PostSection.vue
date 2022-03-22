<template>
  <section class="posts">
    <!-- POPULAR POSTS -->
    <div class="col-4">
      <h3>popular posts</h3>
      <div v-for="el in popularPosts" :key="el.id" class="post-wrapper">
        <figure>
          <img :src="el.imgUrl" :alt="el.title" />
        </figure>
        <div class="info">
          <h4>{{ el.title }}</h4>
          <p>{{ el.date }}</p>
        </div>
      </div>
    </div>
    <!-- RECENT POSTS -->
    <div class="col-4">
      <h3>recent posts</h3>
      <div v-for="el in recentPosts" :key="el.id" class="post-wrapper">
        <figure>
          <img :src="el.imgUrl" :alt="el.title" />
        </figure>
        <div class="info">
          <h4>{{ el.title }}</h4>
          <p>{{ el.date }}</p>
        </div>
      </div>
    </div>
    <!-- FEATURED POSTS | FEATURED AUTHOE -->
    <div class="col-4">
      <!-- FEATURED POSTS -->
      <h3>featured posts</h3>
      <!-- CARD -->
      <div class="card">
        <figure>
          <img src="../assets/img/blog-66.jpg" />
        </figure>
        <div class="overlay">
          <div class="badge">recipes</div>
          <h3>tips to help you quickly prepare your lunch</h3>
        </div>
      </div>
      <!-- FEATURED AUTHOR -->
      <h3>featured author</h3>
      <div class="post-wrapper-big">
        <figure class="avatar">
          <img src="../assets/img/avatar.jpg" />
        </figure>
        <div class="info">
          <h4>john doe</h4>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Amet cum
            placeat est molestias?
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PostSection",
  data() {
    return {
      popularPosts: [
        {
          id: 1,
          title: "simple way to have a pretty face",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-55.jpg`),
        },
        {
          id: 2,
          title: "ranking the greatest players in basketball",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-56.jpg`),
        },
        {
          id: 3,
          title: "4 ways to look cool in glasses",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-57.jpg`),
        },
        {
          id: 4,
          title: "top camper trailer towing tips",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-58.jpg`),
        },
        {
          id: 5,
          title: "5 lovely walks in new york",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-59.jpg`),
        },
      ],
      recentPosts: [
        {
          id: 1,
          title: "main reasons top stop texting and driving",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-65.jpg`),
        },
        {
          id: 2,
          title: "tips to help you quickly prepare your lunch",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-66_1.jpg`),
        },
        {
          id: 3,
          title: "why should i buy a smartwatch?",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-67.jpg`),
        },
        {
          id: 4,
          title: "the best augmented reality smartglasses",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-68.jpg`),
        },
        {
          id: 5,
          title: "12 healthiest foods to eat for breakfast",
          date: "January 12, 2019",
          imgUrl: require(`../assets/img/blog-69.jpg`),
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

.posts {
  min-height: 450px;
  display: flex;
  justify-content: space-between;
  padding: 40px 0;

  .col-4 {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: calc((100% / 3) - 20px);

    h3 {
      padding-bottom: 10px;
      text-transform: uppercase;
      font-weight: bolder;
      color: $dark;
    }

    .post-wrapper {
      height: calc((100% / 5) - 20px);
      display: flex;
      align-items: flex-start;
      gap: 10px;
      cursor: pointer;
      transition: 200ms linear;
      border-bottom: 2px solid $light-border;

      &:hover {
        background: $smoke;
      }

      figure {
        width: 45px;
        aspect-ratio: 1;
      }

      h4 {
        padding-bottom: 3px;
        text-transform: capitalize;
        font-weight: 500;
        color: $mid-grey;
      }

      p {
        text-transform: capitalize;
        font-size: 12px;
        color: $light-grey;
      }
    }

    .card {
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
          background: $cobalto;
        }
      }
    }

    .post-wrapper-big {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      cursor: pointer;
      transition: 200ms linear;

      &:hover {
        background: $smoke;
      }

      .avatar {
        max-width: 100px;
        aspect-ratio: 1;
      }

      h4 {
        padding: 10px 0;
        text-transform: capitalize;
        font-weight: bolder;
        color: $mid-grey;
      }

      p {
        line-height: 18px;
        text-transform: capitalize;
        font-size: 12px;
        color: $light-grey;
      }
    }
  }
}
</style>
