<template>
  <section class="testimonials">
    <div class="graphic-divider py-5">
      <div class="container inner-container h-100 py-5">
        <div class="text-wrapper container d-flex justify-content-center mb-4">
          <div class="text text-center">
            <h2>Our Testimonials</h2>
            <p>
              If you are planning on developing a product landing app or
              website, take a look at this beautiful-crafted
            </p>
          </div>
        </div>
        <div class="cards d-flex justify-content-evenly">
          <div
            class="testimonial-card shadow p-4 mb-5 bg-body rounded pt-5"
            v-for="info in testimonials"
            :key="info"
          >
            <div class="image text-center">
              <img :src="info.img" class="rounded-circle mb-5" alt="" />
            </div>
            <div class="text d-flex justify-content-center mb-3">
              <h5 class="me-2">{{ info.name }}</h5>
              <span> - {{ info.position }}</span>
            </div>
            <p>{{ info.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Testimonials",
  data() {
    return {
      testimonials: [
        {
          img: require("../assets/img/26.jpeg"),
          name: "Julia Ann",
          position: " COO Sofbox",
          description:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium vero eos et consectetur accus adip adip",
        },
        {
          img: require("../assets/img/27.jpeg"),
          name: "Mac Znder",
          position: " Manager Sofbox",
          description:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium vero eos et consectetur accus adip adip",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section.testimonials {
  background-color: $brandLtBlue;
  height: 900px;
  div.graphic-divider {
    background-image: url("../assets/img/15.png");
    background-repeat: repeat-x;
    background-position: left 100% top 0;
    .container {
      div.text-wrapper {
        padding-top: 50px;
        p {
          color: $brandTxtGrey;
        }
        .text {
          width: 45%;
        }
      }
    }
    div.cards {
      .testimonial-card {
        width: 400px;
        img {
          width: 70px;
          border: 1px solid $borderGrey1;
        }
        div.text {
          span {
            color: $brandTxtGrey;
          }
        }
      }
    }
  }
}
</style>
