<template>
  <section
    id="jumbotron"
    class="container d-flex align-items-center rounded p-5 mb-5"
  >
    <div class="text-box ps-2">
      <!-- <h1>{{ jumbotron.title }}</h1> -->
      <h1 class="mb-4">The biggest platform for your growth.</h1>
      <p class="mb-5">
        There are many variations of passages of Lorem ipsum available, but the
        majority have suffered alteration in some form
      </p>
      <button type="button" class="btn text-white px-3">Read More</button>
    </div>
    <div class="jumbotron-img">
      <img :src="jumbotronImg" alt="" class="img-fluid" />
    </div>
  </section>
</template>

<script>
export default {
  name: "JumboTron",
  data() {
    return {
      jumbotronImg: require("../assets/img/27-1.png"),
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section#jumbotron {
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
    p {
      color: $brandTxtGrey;
    }
    button.btn {
      background-color: $brandBlue;
      &:hover {
        background-color: $brandMatteBlack;
      }
    }
  }

  .jumbotron-img {
    position: absolute;
    top: 115px;
    right: 100px;
  }
}
</style>
