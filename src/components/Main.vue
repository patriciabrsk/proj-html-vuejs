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
                <span class="check-icon me-2">
                  <font-awesome-icon icon="fa-solid fa-check" />
                </span>
                <h6>{{ list }}</h6>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="sales container d-flex inner-container">
      <div class="text-wrapper">
        <div class="text">
          <h2>Get tips and tricks on how to skyrocket your sales.</h2>
        </div>
      </div>
      <div class="sales-img">
        <img :src="salesImg" alt="" />
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
      salesImg: require("../assets/img/509.jpeg"),
      marketingList: ["SEO", "SEM", "Website Strategy", "Social Management"],
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
    p {
      color: $brandTxtGrey;
    }
    li {
      h6 {
        display: inline-block;
        font-size: 0.9rem;
      }
      span.check-icon {
        color: $brandBlue;
      }
    }
  }
}
</style>
