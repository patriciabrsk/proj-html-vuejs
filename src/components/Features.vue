<template>
  <section id="features" class="py-5 mb-5">
    <div class="container inner-container py-5">
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
        <div class="row row-cols-4 g-4 mb-5">
          <div class="col" v-for="element in features" :key="element.id">
            <div class="feature-card col p-4 mb-5 rounded gx-3">
              <h5 class="mb-3">{{ element.title }}</h5>
              <font-awesome-icon
                :icon="element.icon"
                :color="element.colorClass"
                size="3x"
                class="py-2 mb-2"
              />
            </div>
          </div>
          <div class="dots"></div>
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
      isHovering: false,
      features: [
        {
          title: "Customized Invoices",
          icon: "fa-solid fa-file-invoice-dollar",
          colorClass: "blue",
        },
        {
          title: "Stock Management",
          icon: "fa-solid fa-arrow-trend-up",
          colorClass: "salmon",
        },
        {
          title: "Receivable & Payables",
          icon: "fa-solid fa-comments-dollar",
          colorClass: "torquoise",
        },
        {
          title: "Manage Buying",
          icon: "fa-solid fa-credit-card",
          colorClass: "blue",
        },
        {
          title: "Powerful & Secure",
          icon: "fa-solid fa-shield-halved",
          colorClass: "salmon",
        },
        {
          title: "Fastest Return Filing",
          icon: "fa-solid fa-folder-open",
          colorClass: "torquoise",
        },
        {
          title: "Monthly Detailed",
          icon: "fa-solid fa-calendar-day",
          colorClass: "blue",
        },
        {
          title: "Product Management",
          icon: "fa-solid fa-list-check",
          colorClass: "salmon",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section#features {
  height: 650px;
  width: 100%;
  background-image: url("../assets/img/14.png");
  background-repeat: no-repeat;
  background-position: -65%;
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
  }
  .cards {
    .feature-card {
      background-color: $white;
      box-shadow: 0 5px 15px rgba(226, 226, 226, 0.685);

      .blue {
        fill: $brandBlue;
      }
      .salmon {
        fill: $brandSalmon;
      }
      .torquoise {
        fill: $brandTorquoise;
      }
    }
  }
}
</style>
