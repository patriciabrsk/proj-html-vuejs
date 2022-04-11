<template>
  <section id="latest">
    <div class="section-wrapper container inner-container">
      <div class="text-wrapper d-flex justify-content-center mb-4 pt-0">
        <div class="text text-center mb-5">
          <h2 class="mb-3">Latest Posts</h2>
          <p>If you are planning on developing a product landing.</p>
        </div>
      </div>
      <div class="cards">
        <div class="row row-cols-3 g-4">
          <div class="col" v-for="post in posts" :key="post.id">
            <div class="post-card rounded p-2">
              <div class="image mb-2">
                <img :src="post.image" alt="" class="img-fluid" />
              </div>
              <div class="text p-4">
                <h5 class="me-2">{{ post.title }}</h5>
                <p>
                  {{ post.text }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Latest",
  data() {
    return {
      posts: [
        {
          image: require("../assets/img/19.jpg"),
          title: "Life Lack Meaning",
          text: "It is a long established fact that a reader will be distracted by the readable",
        },
        {
          image: require("../assets/img/18.jpg"),
          title: "Life Lack Meaning",
          text: "It is a long established fact that a reader will be distracted by the readable",
        },
        {
          image: require("../assets/img/17.jpg"),
          title: "Life Lack Meaning",
          text: "It is a long established fact that a reader will be distracted by the readable",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section#latest {
  height: 500px;
  p {
    color: $brandTxtGrey;
  }
  div.text-wrapper {
    padding-top: 50px;
  }
  div.cards {
    .post-card {
      background-color: $white;
      border: 1px solid $borderGrey3;
    }
  }
}
</style>
