<template>
  <main class="mt-5">
    <Jumbotron />
    <OnlineMarketing />
    <Sales />
    <Features />
    <Testimonials />
    <Latest />

    <Footer />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import OnlineMarketing from "./OnlineMarketing.vue";
import Sales from "./Sales.vue";
import Features from "./Features.vue";
import Testimonials from "./Testimonials.vue";
import Latest from "./Latest.vue";

// import Footer from "./Footer.vue";

export default {
  name: "MyMain",
  components: {
    Jumbotron,
    OnlineMarketing,
    Sales,
    Features,
    Testimonials,
    Latest,
    // Footer,
  },
};
</script>

<style lang="scss" scoped>
main {
  min-width: 1140px;
}
</style>
