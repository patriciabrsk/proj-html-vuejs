<template>
  <section id="testimonials">
    <div class="graphic-divider py-4">
      <div class="container inner-container h-100 py-5">
        <div class="text-wrapper container d-flex justify-content-center mb-4">
          <div class="text text-center mb-5">
            <h2 class="mb-3">Our Testimonials</h2>
            <p>
              If you are planning on developing a product landing app or
              website, take a look at this beautiful-crafted
            </p>
          </div>
        </div>
        <div class="cards d-flex justify-content-around">
          <div
            class="testimonial-card p-4 mb-5 rounded pt-5"
            v-for="info in testimonials"
            :key="info.id"
          >
            <div class="image text-center">
              <img :src="info.img" class="rounded-circle mb-5" alt="" />
            </div>
            <div class="text d-flex justify-content-center mb-4">
              <h5 class="me-2">{{ info.name }}</h5>
              <span> - {{ info.position }}</span>
            </div>
            <p class="pb-2">{{ info.description }}</p>
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

section#testimonials {
  //   background-color: $brandLtBlue;
  background: linear-gradient(360deg, white 0%, $brandLtBlue 100%);
  height: 800px;
  p {
    color: $brandTxtGrey;
  }
  div.graphic-divider {
    background-image: url("../assets/img/15.png");
    background-repeat: no-repeat;
    background-position: left 100% top 0;
    .container {
      div.text-wrapper {
        padding-top: 50px;
        .text {
          width: 45%;
        }
      }
    }
    div.cards {
      .testimonial-card {
        background-color: $white;
        box-shadow: 0 5px 15px rgba(226, 226, 226, 0.685);
        width: 480px;
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
