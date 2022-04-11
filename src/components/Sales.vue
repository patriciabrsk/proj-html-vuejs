<template>
  <section id="sales" class="container d-flex inner-container">
    <div class="text-wrapper me-5">
      <div class="text">
        <h2>Get tips and tricks on how to skyrocket your sales.</h2>
        <p class="py-3">
          Faff about only a quid blower I don't want no agro bleeding chimney
          pot burke tosser cras nice one boot fanny!
        </p>
        <div class="row row-cols-1 d-flex">
          <div
            class="section-card col p-4 d-flex align-items-center rounded"
            v-for="info in sales"
            :key="info.id"
          >
            <div class="icon me-3">
              <img :src="info.iconSrc" alt="" />
            </div>
            <div class="card-text">
              <h5>{{ info.title }}</h5>
              <p>{{ info.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="sales-img">
      <img :src="salesImg" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Sales",
  data() {
    return {
      salesImg: require("../assets/img/509.jpeg"),
      sales: [
        {
          title: "Reporting Analysis",
          text: "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.",
          iconSrc: require("../assets/img/510.png"),
        },
        {
          title: "Technical SEO Audit",
          text: "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.",
          iconSrc: require("../assets/img/511.png"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section#sales {
  p {
    color: $brandTxtGrey;
  }
  div.text-wrapper {
    div.text {
      div.section-card {
        border: 1px solid transparent;
        &:hover {
          border: 1px solid $borderGrey1;
          box-shadow: 0 5px 15px rgba($grey, 0.685);
          //   box-shadow: 0 5px 15px rgba(226, 226, 226, 0.685);
          cursor: pointer;
        }
        .card-text:hover h5 {
          color: $brandBlue;
        }
      }
    }
  }
}
</style>
