<template>
  <div class="container-fluid">
    <div class="container">
      <div class="badge-wrapper">
        <div class="triangle"></div>
        <div class="badge">Get in Touch</div>
      </div>
      <div class="col large">
        <h4>about the blog</h4>
        <p v-for="el in lorem" :key="el.id">
          {{ el.text }}
        </p>
        <h4 class="link">
          view more <i class="fa-solid fa-chevron-right"></i>
        </h4>
      </div>
      <div class="col">
        <h4>recent posts</h4>
        <div class="post-wrapper">
          <div v-for="el in posts" :key="el.id" class="post">
            <figure class="picture">
              <img :src="el.imgUrl" :alt="el.id" />
            </figure>
            <div class="post-details">
              <p class="content">
                {{ el.text }}
              </p>
              <p class="date">
                {{ el.date }}
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="col">
        <h4>recent comments</h4>
      </div>
      <div class="col">
        <h4>categories</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FirstFooterSection",
  data() {
    return {
      lorem: [
        {
          id: 1,
          text: "Lorem ipsum dolor sit amet, consecteur adipiscing elit. Donec eu pulvinar magna semper scelerisque.",
        },
        {
          id: 2,
          text: "Praesent veneratis turpis vitae purus semper, eget sagittis velit venenatis ptent taciti sociosqu ad litora...",
        },
      ],
      posts: [
        {
          id: 1,
          imgUrl: require(`../assets/img/our-office-4-square.jpg`),
          text: "Lorem ipsum dolor sit, consectetur adipiscing elit.",
          date: "12:53 AM Dec 19th",
        },
        {
          id: 2,
          imgUrl: require(`../assets/img/our-office-5-square.jpg`),
          text: "Lorem ipsum dolor sit, consectetur adipiscing elit.",
          date: "12:53 AM Dec 19th",
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
  background: $dark-bkg;

  .container {
    @include container;
    padding: 60px 0;
    display: flex;
    position: relative;

    .badge-wrapper {
      display: flex;
      cursor: default;
      position: absolute;
      top: -13px;

      .triangle {
        width: 0;
        height: 0;
        border-style: solid;
        border-width: 0 0 13px 10px;
        border-color: transparent transparent #005580 transparent;
      }

      .badge {
        padding: 5px 15px;
        font-family: "Shadows Into Light", cursive;
        font-size: 18px;
        user-select: none;
        color: $smoke;
        background: $cobalto;
      }
    }

    .col {
      width: 23%;
      min-height: 240px;
      padding-right: 15px;
      font-size: 12px;
      border: 2px dashed yellow;

      h4 {
        text-transform: uppercase;
        font-weight: bolder;
        color: $smoke;
      }

      .post-wrapper {
        display: flex;
        flex-direction: column;
        gap: 15px;
        padding: 10px 0;

        .post {
          display: flex;
          align-items: center;

          .picture {
            width: 70px;
            margin-right: 10px;
            border-radius: 50%;
            overflow: hidden;
          }

          .post-details {
            flex-grow: 1;

            .content {
              cursor: pointer;
              color: $smoke;

              &:hover {
                text-decoration: underline;
              }
            }

            .date {
              padding: 8px 0;
              color: $light-grey;
            }
          }
        }
      }
    }

    .large {
      flex-grow: 1;

      p {
        padding: 10px 0;
        line-height: 25px;
        color: $light-grey;
      }

      .link {
        cursor: pointer;

        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
}
</style>
