<template>
  <div class="col-10">
    <div
      v-for="el in contents"
      :key="el.id"
      class="content-box"
      :class="el.large == true ? 'large' : ''"
    >
      <figure class="picture">
        <img :src="el.imgUrl" :alt="el.title" />
      </figure>
      <div class="info-wrapper">
        <div class="date">
          <div class="day">{{ el.day }}</div>
          <div class="month">{{ el.month }}</div>
        </div>
        <div class="description">
          <h2>{{ el.title }}</h2>
          <p>{{ el.text }}</p>
          <div class="wrapper">
            <div class="details">
              <div class="author">
                <i class="fa-regular fa-user"></i>
                {{ el.author }}
              </div>
              <div class="category">
                <i class="fa-regular fa-folder"></i>
                {{ el.category }}
              </div>
              <div class="comments">
                <i class="fa-regular fa-comment-dots"></i>
                {{ el.comments }}
              </div>
            </div>
            <div class="button">
              {{ el.button }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainColLarge",
  data() {
    return {
      contents: [
        {
          id: 1,
          title: "how to make friends as a grown-up",
          text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga corrupti quia modi incidunt cumque perspiciatis provident labore corporis nostrum odio velit sed neque, tenetur officia est, id aliquam aut eveniet nesciunt unde! Maxime maiores, fugiat itaque sunt ut consectetur nulla, autem voluptatibus quod quas adipisci officia suscipit amet omnis ratione.",
          day: "12",
          month: "jan",
          author: "by john doe",
          category: "lifestyle, travel",
          comments: "12 comments",
          button: "read more",
          large: false,
          imgUrl: require(`../assets/img/blog-54.jpg`),
        },
        {
          id: 2,
          title: "simple ways to have a pretty face",
          text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga corrupti quia modi incidunt cumque perspiciatis provident labore corporis nostrum odio velit sed neque, tenetur officia est, id aliquam aut eveniet nesciunt unde! Maxime maiores, fugiat itaque sunt ut consectetur nulla, autem voluptatibus quod quas adipisci officia suscipit amet omnis ratione.",
          day: "12",
          month: "jan",
          author: "by john doe",
          category: "photography, travel",
          comments: "12 comments",
          button: "read more",
          large: false,
          imgUrl: require(`../assets/img/blog-55_1.jpg`),
        },
        {
          id: 3,
          title: "ranking the greatest players in basketball",
          text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga corrupti quia modi incidunt cumque perspiciatis provident labore corporis nostrum odio velit sed neque, tenetur officia est, id aliquam aut eveniet nesciunt unde! Maxime maiores, fugiat itaque sunt ut consectetur nulla, autem voluptatibus quod quas adipisci officia suscipit amet omnis ratione.",
          day: "12",
          month: "jan",
          author: "by john doe",
          category: "sports, business",
          comments: "12 comments",
          button: "read more",
          large: false,
          imgUrl: require(`../assets/img/blog-56_1.jpg`),
        },
        {
          id: 4,
          title: "top camper trailer towing tips",
          text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga corrupti quia modi incidunt cumque perspiciatis provident labore corporis nostrum odio velit sed neque, tenetur officia est, id aliquam aut eveniet nesciunt unde! Maxime maiores, fugiat itaque sunt ut consectetur nulla, autem voluptatibus quod quas adipisci officia suscipit amet omnis ratione.",
          day: "12",
          month: "jan",
          author: "by john doe",
          category: "lifestyle, travel",
          comments: "12 comments",
          button: "read more",
          large: false,
          imgUrl: require(`../assets/img/blog-58_1.jpg`),
        },
        {
          id: 5,
          title: "10 best travel tips after 5 years traveling the world",
          text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fuga corrupti quia modi incidunt cumque perspiciatis provident labore corporis nostrum odio velit sed neque, tenetur officia est, id aliquam aut eveniet nesciunt unde! Maxime maiores, fugiat itaque sunt ut consectetur nulla, autem voluptatibus quod quas adipisci officia suscipit amet omnis ratione.",
          day: "8",
          month: "jan",
          author: "by john doe",
          category: "lifestyle, travel",
          comments: "12 comments",
          button: "read more",
          large: true,
          smallImages: [
            {
              imgUrl: require(`../assets/img/blog-13.jpg`),
            },
            {
              imgUrl: require(`../assets/img/blog-16.jpg`),
            },
            {
              imgUrl: require(`../assets/img/blog-20.jpg`),
            },
            {
              imgUrl: require(`../assets/img/blog-23.jpg`),
            },
            {
              imgUrl: require(`../assets/img/blog-29.jpg`),
            },
            {
              imgUrl: require(`../assets/img/blog-40.jpg`),
            },
          ],
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

.col-10 {
  width: 75%;
  display: flex;
  flex-direction: column;
  gap: 40px;
  padding: 40px 0;

  .large {
    background: rebeccapurple;
  }

  .content-box {
    border-bottom: 2px solid $light-border;

    .picture {
      height: 400px;
      cursor: pointer;
      transition: 200ms linear;

      &:hover {
        filter: brightness(0.8);
      }
    }

    .info-wrapper {
      min-height: 130px;
      display: flex;

      .date {
        flex-shrink: 0;
        width: 60px;
        display: flex;
        flex-direction: column;
        align-items: center;
        font-size: 10px;
        font-weight: bolder;
        text-transform: capitalize;
        padding: 20px 0;

        .day {
          width: 30px;
          height: 30px;
          display: flex;
          justify-content: center;
          align-items: center;
          background: $smoke;
        }

        .month {
          width: 30px;
          height: 20px;
          display: flex;
          justify-content: center;
          align-items: center;
          color: $smoke;
          background: $dark-bkg;
        }
      }

      .description {
        flex-grow: 1;
        padding: 20px 0;

        h2 {
          text-transform: capitalize;
          cursor: pointer;
          color: $dark;

          &:hover {
            text-decoration: underline;
          }
        }

        p {
          line-height: 22px;
          padding: 10px 0;
          color: $light-grey;
        }

        .wrapper {
          display: flex;
          justify-content: space-between;
          align-items: center;
          padding-top: 5px;
          text-transform: capitalize;
          color: $light-grey;

          .details {
            display: flex;
            gap: 30px;

            .author,
            .category,
            .comments {
              cursor: pointer;

              &:hover {
                color: $dark;
                text-decoration: underline;
              }
            }
          }

          .button {
            padding: 5px 10px;
            border-radius: 5px;
            border: 1px solid $light-grey;
            cursor: pointer;
            transition: 200ms linear;

            &:hover {
              color: $smoke;
              background: $cobalto;
            }
          }

          i {
            padding-right: 5px;
          }
        }
      }
    }
  }
}
</style>
