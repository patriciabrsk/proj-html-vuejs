<template>
  <footer
    class="container-fluid border-top d-flex justify-content-center mb-5 d-flex"
  >
    <div
      class="row container justify-content-evenly d-flex inner-container my-5"
    >
      <div class="col">
        <img src="../assets/img/35.png" alt="Sofbox logo" class="mb-4" />
        <p class="mb-5">
          It is a long established fact that a reader will be distracted by the
          readable content
        </p>
        <p class="pt-4">
          Copyright &copy; 2018 <span class="fw-normal">Sofbox</span>
        </p>
      </div>
      <div
        class="col d-flex justify-content-center"
        v-for="link in footerLinks"
        :key="link"
      >
        <div class="content">
          <h5 class="mb-4">{{ link.title }}</h5>
          <ul class="list-unstyled">
            <li class="mb-3">{{ link.link1 }}</li>
            <li class="mb-3">{{ link.link2 }}</li>
            <li class="mb-3">{{ link.link3 }}</li>
            <li class="mb-3">{{ link.link4 }}</li>
            <li class="mb-3">{{ link.link5 }}</li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "MyFooter",
  data() {
    return {
      footerLinks: [
        {
          title: "Menu",
          link1: "About Us",
          link2: "Theme",
          link3: "Features",
          link4: "Pricing",
          link5: "Blog",
        },
        {
          title: "About Us",
          link1: "About Sofbox",
          link2: "Roadmap",
          link3: "How it Works",
          link4: "Team",
          link5: "News",
        },
        {
          title: "Quick Links",
          link1: "About Us",
          link2: "Theme",
          link3: "Features",
          link4: "Pricing",
          link5: "Blog",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

p,
li {
  color: $brandTxtGrey;
}

span {
  color: $brandBlue;
}
</style>
