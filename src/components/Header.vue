<template>
  <header class="pt-2 container wv-100">
    <nav class="navbar d-flex justify-content-between align-items-center">
      <div class="nav-logo">
        <img :src="logo" alt="logo" />
      </div>
      <div
        class="nav-leftside d-flex align-items-center justify-content-between"
      >
        <ul class="nav-links d-flex mb-0 ps-0 me-2">
          <li
            v-for="(link, index) in headerLinks"
            :key="index"
            class="list-unstyled me-4"
          >
            <a
              class="text-decoration-none"
              :class="{ active: link.current }"
              :href="link.url"
              ><h6 class="m-0">{{ link.text }}</h6>
            </a>
          </li>
        </ul>
        <div class="icons d-flex me-5">
          <font-awesome-icon icon="fa-solid fa-magnifying-glass" class="me-3" />
          <font-awesome-icon
            icon="fa-solid fa-cart-shopping position-relative"
          />
        </div>
        <div class="button">
          <button type="button" class="btn text-white px-3">Get Started</button>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "MyHeader",
  data() {
    return {
      logo: require("../assets/img/logo-2.png"),
      headerLinks: [
        {
          text: "Home",
          url: "#",
          current: true,
        },
        {
          text: "About Us",
          url: "#",
          current: false,
        },
        {
          text: "Feature",
          url: "#",
          current: false,
        },
        {
          text: "Testimonials",
          url: "#",
          current: false,
        },
        {
          text: "Contact Us",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/style/style.scss";

header {
  height: 50px;
  img {
    width: 50px;
  }
  .nav-leftside {
    ul.nav-links {
      li {
        &:active,
        &.active {
          border-bottom: 3px solid blue;
        }
        a {
          color: #495057;
        }
      }
    }
    button {
      background-color: $brandBlue;
    }
  }
}
</style>
