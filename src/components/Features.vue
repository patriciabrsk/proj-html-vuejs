<template>
  <section class="features">
    <div class="container inner-container">
      <div class="text-wrapper d-flex justify-content-between mb-5">
        <div class="texts">
          <h2 class="mb-3">Popular features that your business needs</h2>
          <p class="w-75">
            Faff about only a quid blower I don't want no agro bleeding chimney
            pot burke tosser cras nice one boot fanny!
          </p>
        </div>
        <button type="button" class="btn align-self-center text-white px-3">
          Explore More Feature
        </button>
      </div>
      <div class="cards">
        <div class="row row-cols-4 g-4">
          <div
            class="shadow col p-3 bg-body rounded"
            v-for="element in features"
            :key="element.id"
          >
            <h5>{{ element.title }}</h5>
            <img src="" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Features",
  data() {
    return {
      features: [
        {
          title: "Customized Invoices",
          img: require("../assets/img/510.png"),
        },
        {
          title: "Stock Management",
          img: require("../assets/img/510.png"),
        },
        {
          title: "Receivable & Payables",
          img: require("../assets/img/510.png"),
        },
        {
          title: "Manage Buying",
          img: require("../assets/img/510.png"),
        },
        {
          title: "Powerful & Secure",
          img: require("../assets/img/510.png"),
        },
        {
          title: "Fastest Return Filing",
          img: require("../assets/img/510.png"),
        },
        {
          title: "Monthly Detailed",
          img: require("../assets/img/510.png"),
        },
        {
          title: "Product Management",
          img: require("../assets/img/510.png"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section.features {
  .text-wrapper {
    button.btn {
      background-color: $brandBlue;
    }
    .texts {
      p {
        color: $brandTxtGrey;
        width: 60%;
      }
    }
    button {
    }
  }
}
</style>
