<template>
  <main class="mt-5 container">
    <section
      class="jumbotron container d-flex align-items-center rounded-3 p-5 mb-5"
    >
      <div class="text-box ps-2">
        <!-- <h1>{{ jumbotron.title }}</h1> -->
        <h1 class="mb-4">The biggest platform for your growth.</h1>
        <p class="mb-5">
          There are many variations of passages of Lorem ipsum available, but
          the majority have suffered alteration in some form
        </p>
        <button type="button" class="btn text-white px-3">Read More</button>
      </div>
      <div class="jumbotron-img">
        <img :src="jumbotronImg" alt="" class="img-fluid" />
      </div>
    </section>

    <section class="online-marketing container inner-container">
      <div class="row row-cols-3 d-flex py-5">
        <div
          class="d-flex flex-row col section-card mt-5 px-0"
          v-for="index in 3"
          :key="index"
        >
          <div class="icon me-4">
            <img :src="marketingImg" alt="" class="img-fluid" />
          </div>
          <div class="text">
            <h5>Online Marketing</h5>
            <p class="mb-4">
              It is a long established fact that a reader will be distracted.
            </p>
            <ul class="p-0">
              <li
                class="list-unstyled"
                v-for="list in marketingList"
                :key="list"
              >
                <span class="check-icon me-3">
                  <font-awesome-icon icon="fa-solid fa-check" />
                </span>
                <span>{{ list }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="sales container d-flex inner-container">
      <div class="text-wrapper me-4">
        <div class="text">
          <h2>Get tips and tricks on how to skyrocket your sales.</h2>
          <p class="py-3">
            Faff about only a quid blower I don't want no agro bleeding chimney
            pot burke tosser cras nice one boot fanny!
          </p>
          <div class="row row-cols-1 d-flex">
            <div
              class="section-card col p-4 d-flex align-items-center"
              v-for="(value, index) in sales"
              :key="index"
            >
              <div
                class="icon me-3"
                v-for="(image, index) in sales"
                :key="index"
              >
                <img :src="image.iconsSrc[index]" alt="" />
              </div>
              <div class="card-text">
                <h5>{{ value.title[index] }}</h5>
                <p>{{ value.text }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="sales-img">
        <img :src="salesImg" alt="" />
      </div>
    </section>

    <section class="features">
      <div class="container inner-container">
        <div class="text-wrapper d-flex justify-content-between">
          <div class="text-info">
            <h2>Popular features that your business needs</h2>
            <p>
              Faff about only a quid blower I don't want no agro bleeding pot
              burke tosser cras nice one boot fanny!
            </p>
          </div>
          <button type="button" class="btn text-white px-3">
            Explore More Feature
          </button>
        </div>
        <div class="cards">
          <div
            class="shadow p-3 mb-5 bg-body rounded"
            v-for="card in features"
            :key="card"
          ></div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "MyMain",
  data() {
    return {
      jumbotronImg: require("../assets/img/27-1.png"),
      marketingImg: require("../assets/img/24.png"),
      marketingList: ["SEO", "SEM", "Website Strategy", "Social Management"],
      salesImg: require("../assets/img/509.jpeg"),
      sales: [
        {
          title: ["Reporting Analysis", "Technical SEO Audit"],
          text: "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.",
          iconsSrc: [
            require("../assets/img/510.png"),
            require("../assets/img/511.png"),
          ],
        },
      ],
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
      //   jumbotron: [
      //     {
      //       title: "The biggest platform for your growth",
      //       text: "There are many variations of passages of Lorem ipsum available, but the majority have suffered alteration in some form",
      //       img: require("../assets/img/27-1.png"),
      //     },
      //   ],
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
  p {
    color: $brandTxtGrey;
  }
  section.jumbotron {
    background-color: #f2f7ff;
    height: 400px;

    .section-card {
      width: 200px;
    }
    div.text-box {
      width: 40%;
      h1 {
        font-size: 3rem;
      }
    }

    .jumbotron-img {
      position: absolute;
      top: 115px;
      right: 100px;
    }
    button {
      background-color: $brandBlue;
    }
  }

  section.online-marketing {
    height: 400px;

    div.icon {
      width: 18%;
    }
    div.text {
      width: 60%;
      li {
        span {
          display: inline-block;
          font-weight: bold;
          font-size: 0.9rem;
        }
        span.check-icon {
          color: $brandBlue;
        }
      }
    }
  }

  section.sales {
    div.text-wrapper {
      div.text {
        div.section-card {
          &:hover {
            color: $brandBlue;
            border: 1px solid $borderGrey1;
          }
        }
      }
    }
  }
}
</style>
