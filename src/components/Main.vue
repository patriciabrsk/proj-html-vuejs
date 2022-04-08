<template>
  <main class="mt-5 container">
    <Jumbotron />
    <OnlineMarketing />
    <Sales />
    <Features />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import OnlineMarketing from "./OnlineMarketing.vue";
import Sales from "./Sales.vue";
import Features from "./Features.vue";

export default {
  name: "MyMain",
  components: { Jumbotron, OnlineMarketing, Sales, Features },
};
</script>

<style lang="scss" scoped></style>
