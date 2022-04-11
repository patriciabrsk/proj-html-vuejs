<template>
  <section class="testimonials">
    <div class="container inner-container h-100">
      <div class="text-wrapper container d-flex justify-content-center mb-4">
        <div class="text text-center">
          <h2>Our Testimonials</h2>
          <p>
            If you are planning on developing a product landing app or website,
            take a look at this beautiful-crafted
          </p>
        </div>
      </div>
      <div class="cards d-flex justify-content-evenly">
        <div class="testimonial-card shadow p-4 mb-5 bg-body rounded">ciao</div>
        <div class="testimonial-card shadow p-4 mb-5 bg-body rounded">ciao</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Testimonials",
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section.testimonials {
  height: 100%;
  background-image: url("../assets/img/15.png");
  background-repeat: no-repeat;
  .container {
    div.text-wrapper {
      p {
        color: $brandTxtGrey;
      }
      .text {
        width: 40%;
      }
    }
  }
}
</style>
