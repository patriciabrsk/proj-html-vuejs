<template>
  <section id="contact" class="py-5 h-100 my-5">
    <div class="section-wrapper container inner-container py-5 mt-5">
      <div class="text-wrapper d-flex justify-content-center mb-4 pt-0">
        <div class="text text-center mb-5">
          <h2 class="mb-3">Contact with our team</h2>
          <p>If you are planning on developing a product landing.</p>
        </div>
      </div>
      <div class="content d-flex jsutify-content-between">
        <div class="map w-50">
          <div class="image mb-2">
            <img
              src="../../assets/img/StaticMapService.GetMapIma.png"
              alt="Map"
              class="img-fluid"
            />
          </div>
        </div>
        <div class="contact-area px-4 w-50">
          <div class="logo mb-5">
            <img src="../../assets/img/35.png" alt="Sofbox logo" />
          </div>
          <div class="contact-info mb-5">
            <h5 class="mb-3">9840 Shore St. Fond Du Lac, WI 54935</h5>
            <p class="phone-number mb-0">0 1223 456 789</p>
            <span class="email">mail@sofbox.com</span>
          </div>
          <div class="socials d-flex py-2 mb-5">
            <div class="fb px-2 py-1 rounded border me-2">
              <img src="../../assets/img/facebook.png" alt="Facebook logo" />
            </div>
            <div class="twitter p-2 rounded border me-2">
              <img src="../../assets/img/twitter.png" alt="Twitter logo" />
            </div>
            <div class="twitter px-2 py-1 rounded border me-2">GH</div>
            <div class="twitter px-2 py-1 rounded border me-2">IG</div>
          </div>
          <h4 class="mb-3">Get in Touch</h4>
          <div class="contact-input mb-5">
            <div class="row d-flex justify-content-between w-100 mb-4">
              <div class="col-6">
                <input
                  type="text"
                  id="name"
                  placeholder="Your name"
                  class="form-control"
                />
              </div>
              <div class="col-6">
                <input
                  type="text"
                  id="email"
                  placeholder="Your email"
                  class="form-control"
                />
              </div>
            </div>
            <div class="row mb-4">
              <div class="col-12">
                <input
                  type="text"
                  id="email"
                  placeholder="Your subject"
                  class="form-control"
                />
              </div>
            </div>
            <textarea
              class="form-control mb-4"
              placeholder="Your Message"
              v-model="newMessage"
              id="text-area"
              rows="8"
            ></textarea>
            <button type="submit" class="btn text-white px-3">
              Send Message
            </button>
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
  data() {
    return {
      newMessage: "",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/style.scss";

section#contact {
  height: 600px;
  p,
  span {
    color: $brandTxtGrey;
  }
  button {
    background-color: $brandBlue;
  }
  div.content {
    .contact-area {
      .socials {
        img {
          width: 18px;
          color: $brandBlue;
        }
      }
    }
  }
}
</style>
