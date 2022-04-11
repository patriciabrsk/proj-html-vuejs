<template>
  <section id="contact" class="py-5 mt-5">
    <div class="section-wrapper container inner-container py-5 mt-5">
      <div class="text-wrapper d-flex justify-content-center mb-4 pt-0">
        <div class="text text-center mb-5">
          <h2 class="mb-3">Contact with our team</h2>
          <p>If you are planning on developing a product landing.</p>
        </div>
      </div>
      <div class="content d-flex jsutify-content-between">
        <div class="map">
          <div class="image mb-2">
            <img
              src="../assets/img/StaticMapService.GetMapIma.png"
              alt="Map"
              class="img-fluid"
            />
          </div>
        </div>
        <div class="contact-area px-4">
          <div class="logo mb-5">
            <img src="../assets/img/35.png" alt="Sofbox logo" />
          </div>
          <div class="contact-info">
            <h5 class="mb-3">9840 Shore St. Fond Du Lac, WI 54935</h5>
            <p class="phone-number mb-0">0 1223 456 789</p>
            <span class="email">mail@sofbox.com</span>
          </div>
          <div class="socials">
            <div class="fb p-3 border">FB</div>
            <div class="twitter p-3 border">TW</div>
            <div class="twitter p-3 border">GH</div>
            <div class="twitter p-3 border">IG</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Contact",
};
</script>

<style lang="scss" scoped>
@import "../assets/style/style.scss";

section#contact {
  height: 600px;
  p,
  span {
    color: $brandTxtGrey;
  }
}
</style>
