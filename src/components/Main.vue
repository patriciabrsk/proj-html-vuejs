<template>
  <main class="mt-5 container">
    <Jumbotron />
    <OnlineMarketing />
    <Sales />

    <section class="features">
      <div class="container inner-container">
        <div class="text-wrapper d-flex justify-content-between mb-5">
          <div class="texts">
            <h2 class="mb-3">Popular features that your business needs</h2>
            <p class="w-75">
              Faff about only a quid blower I don't want no agro bleeding
              chimney pot burke tosser cras nice one boot fanny!
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
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import OnlineMarketing from "./OnlineMarketing.vue";
import Sales from "./Sales.vue";

export default {
  name: "MyMain",
  components: { Jumbotron, OnlineMarketing, Sales },
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

      //   marketing: [
      //     {
      //       img: require("../assets/img/24.png"),
      //       title: "Online Marketing",
      //       text: "It is a long established fact that a reader will be distracted.",
      //       list: ["SEO", "SEM", "Website Strategy", "Social Management"],
      //     },
      //   ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";
main {
  button.btn {
    background-color: $brandBlue;
  }
  p {
    color: $brandTxtGrey;
  }
  //   section.jumbotron {
  //     background-color: #f2f7ff;
  //     height: 400px;

  //     .section-card {
  //       width: 200px;
  //     }
  //     div.text-box {
  //       width: 40%;
  //       h1 {
  //         font-size: 3rem;
  //       }
  //     }

  //     .jumbotron-img {
  //       position: absolute;
  //       top: 115px;
  //       right: 100px;
  //     }
  //   }

  //   section.online-marketing {
  //     height: 400px;

  //     div.icon {
  //       width: 18%;
  //     }
  //     div.text {
  //       width: 60%;
  //       li {
  //         span {
  //           display: inline-block;
  //           font-weight: bold;
  //           font-size: 0.9rem;
  //         }
  //         span.check-icon {
  //           color: $brandBlue;
  //         }
  //       }
  //     }
  //   }

  section.sales {
    div.text-wrapper {
      div.text {
        div.section-card {
          border: 1px solid transparent;
          &:hover {
            color: $brandBlue;
            border: 1px solid $borderGrey1;
          }
        }
      }
    }
  }

  section.features {
    .text-wrapper {
      .text-info {
        p {
          width: 60%;
        }
      }
      button {
      }
    }
  }
}
</style>
