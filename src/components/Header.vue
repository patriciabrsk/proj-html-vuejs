<template>
  <header>
    <nav
      class="navbar container d-flex justify-content-between align-items-center"
    >
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
            class="list-unstyled me-4 py-2 fw-normal"
            :class="{ active: link.current }"
            @click="toggle()"
          >
            <a
              class="text-decoration-none"
              :href="link.url"
              :class="{ active: link.current }"
              @click="toggle()"
              >{{ link.text }}
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
      isClicked: false,
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
  methods: {
    toggle() {
      this.link.current = !this.link.current;
      this.isClicked = !this.isClicked;
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/style/style.scss";

header {
  height: 50px;
  nav.navbar {
    padding: 20px 120px;
    img {
      width: 45px;
    }
  }
  .nav-leftside {
    ul.nav-links {
      li {
        border-bottom: 3px solid transparent;
        color: $brandTxtDarkGrey;
        &:hover,
        &.active {
          color: $brandBlue;
          border-bottom: 3px solid $brandBlue;
        }
        a {
          font-weight: 500;
          color: $brandTxtDarkGrey;
          &:hover,
          &.active {
            color: $brandBlue;
          }
        }
      }
    }
    button {
      background-color: $brandBlue;
    }
  }
}
</style>
