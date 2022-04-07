<template>
  <main class="mt-5 container">
    <section
      class="jumbotron container d-flex align-items-center rounded-3 p-5"
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
      <div class="jumbotron-img position absolute">
        <img :src="jumbotronImg" alt="" class="img-fluid" />
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
      //   jumbotron: [
      //     {
      //       title: "The biggest platform for your growth",
      //       text: "There are many variations of passages of Lorem ipsum available, but the majority have suffered alteration in some form",
      //       img: require("../assets/img/27-1.png"),
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
  height: 425px;
  .text-box {
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
</style>
