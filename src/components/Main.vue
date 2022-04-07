<template>
  <main class="mt-5">
    <section class="jumbotron d-flex rounded-3 p-5">
      <div class="text-box w-50">
        <!-- <h1>{{ jumbotron.title }}</h1> -->
        <h1>The biggest platform for your growth</h1>
        <p>
          There are many variations of passages of Lorem ipsum available, but
          the majority have suffered alteration in some form
        </p>
        <button type="button" class="mt-3 btn text-white px-3">
          Read More
        </button>
      </div>
      <div class="jumbotron-img position-absolute top-10 start-70">
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
  height: 100%;
  width: 100%;
  background-color: #f2f7ff;
  .text-box {
    height: 300px;
  }

  .jumbotron-img {
  }
  button {
    background-color: $brandBlue;
  }
}
</style>
