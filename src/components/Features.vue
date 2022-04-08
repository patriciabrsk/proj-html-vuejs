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
            class="feature col p-3 h-100 rounded"
            v-for="element in features"
            :key="element.id"
          >
            <h5>{{ element.title }}</h5>
            <font-awesome-icon :icon="element.icon" size="lg" />
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
          icon: "fa-solid fa-file-invoice-dollar",
        },
        {
          title: "Stock Management",
          icon: "fa-solid fa-arrow-trend-up",
        },
        {
          title: "Receivable & Payables",
          icon: "fa-solid fa-comments-dollar",
        },
        {
          title: "Manage Buying",
          icon: "fa-solid fa-credit-card",
        },
        {
          title: "Powerful & Secure",
          icon: "fa-solid fa-shield-halved",
        },
        {
          title: "Fastest Return Filing",
          icon: "fa-solid fa-folder-open",
        },
        {
          title: "Monthly Detailed",
          icon: "fa-solid fa-calendar-day",
        },
        {
          title: "Product Management",
          icon: "fa-solid fa-list-check",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section.features {
  background-image: url("../assets/img/14.png");
  background-repeat: no-repeat;
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
    .cards {
      .feature {
        background-color: $white;
        box-shadow: 0 5px 15px rgba(235, 235, 235, 0.685);
      }
    }
  }
}
</style>
