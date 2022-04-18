<template>
  <main class="mt-5">
    <Jumbotron />
    <OnlineMarketing />
    <Sales />
    <Features />
    <Testimonials />
    <Latest />
    <Contact />
    <Footer />
  </main>
</template>

<script>
import Jumbotron from "./Main/Jumbotron.vue";
import OnlineMarketing from "./Main/OnlineMarketing.vue";
import Sales from "./Main/Sales.vue";
import Features from "./Main/Features.vue";
import Testimonials from "./Main/Testimonials.vue";
import Latest from "./Main/Latest.vue";
import Contact from "./Main/Contact.vue";

export default {
  name: "MyMain",
  components: {
    Jumbotron,
    OnlineMarketing,
    Sales,
    Features,
    Testimonials,
    Latest,
    Contact,
  },
};
</script>

<style lang="scss" scoped>
main {
  min-width: 1140px;
}
</style>
