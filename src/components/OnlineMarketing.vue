<template>
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
            <li class="list-unstyled" v-for="list in marketingList" :key="list">
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
</template>

<script>
export default {
  name: "OnlineMarketing",
  data() {
    return {
      marketingImg: require("../assets/img/24.png"),
      marketingList: ["SEO", "SEM", "Website Strategy", "Social Management"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

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
</style>
