<template>
  <footer id="contact" class="container pt-5  pb-5 text-muted"  style="margin-top:-5px">
    <div class="container" data-aos="zoom-in-up">
        <h2 class="mb-5 text-muted text-center font-weight-bolder">Contact Me</h2>
        <div class="row">
            <div class="col-md-5 mb-4">
                <h4 class="text-muted mb-2">Contact Info</h4>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3863.707939520336!2d121.44597041449683!3d14.443987684768583!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3397f1e22a2de2eb%3A0xc81ceec28a4955b2!2sBrgy.%20Bulihan%20Famy%2C%20Laguna!5e0!3m2!1sen!2sph!4v1596293942003!5m2!1sen!2sph"  class="w-100 h-50" width="400" height="300" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                <div class="third-text-color py-3">
                    <p class="text-lg text-muted">
                      <i class="fas fa-map-marker-alt mr-3"></i> Lilian st. Brgy. Bulihan Famy, Laguna
                    </p>
                    <p class="text-lg">
                      <i class="fa fa-envelope mr-3"></i>
                      <a class="text-muted" href="mailto:celisinan@gmail.com">celisinan@gmail.com</a>
                    </p>
                    <p class="text-lg text-muted">
                      <i style="transform: rotate(100deg)" class="fas fa-phone  mr-3"></i> +639268421554<br>
                    </p>
                    <p class="text-lg">
                      <i class="fas fa-globe-asia mr-3"></i>
                      <a class="text-muted" href="/">this.website.com</a>
                    </p>
                </div>
            </div>
            <div class="col-md-7">
              <form @submit.prevent="send" class="needs-validation" novalidate>
                  <div class="row">
                      <div class="col-md-6 mb-3">
                          <label for="firstName">First name</label>
                          <input type="text" class="form-control" id="firstName" v-model="form.firstname" placeholder="" value="" required>
                          <div class="invalid-feedback">
                            Valid first name is required.
                          </div>
                      </div>
                      <div class="col-md-6 mb-3">
                          <label for="lastName">Last name</label>
                          <input type="text" class="form-control" id="lastName" v-model="form.lastname" placeholder="" value="" required>
                          <div class="invalid-feedback">
                            Valid last name is required.
                          </div>
                      </div>
                  </div>
                  <div class="mb-3">
                        <label for="email">Email</label>
                        <input type="email" class="form-control" id="email" v-model="form.email" placeholder="you@example.com" required>
                        <div class="invalid-feedback">
                          Please enter a valid email address.
                        </div>
                  </div>
                  <div class="row mb-3">
                      <div class="col-md-12">
                          <div class="form-group">
                              <label for="description">Your Message</label>
                              <textarea class="form-control" id="message" v-model="form.message" rows="3" required></textarea>
                              <div class="invalid-feedback">
                                  Valid message is required, say something to Inan.
                              </div>
                          </div>
                      </div>
                  </div>
                  <button class="btn btn-lg btn-block btn-dark" type="submit">Send Message</button>
              </form>
          </div>
        </div>
        <div class="mt-3 mb-3">
            <h3 class="text-center">Social Media</h3>
            <div class="row justify-content-center footer-social">
                <a v-for="(data, index) in social" :key="index" :href="data.url" target="__blank">
                  <i :class="'fab '+ data.icon"></i>
                </a>
            </div>
        </div>
        <div class=" col-md-8 offset-md-2 text-center">
            <b>
              &copy;{{ new Date().getFullYear() }}
              Inan. All Rights Reserved.
            </b>
        </div>
        <div class="col-md-8 offset-md-2 text-center " >
            <nuxt-link class="logo-name dark-text" :to="{ name: 'index' }">Inan</nuxt-link>
        </div>
    </div>
  </footer>
</template>
<script>
export default {
  name:'Foot',
  props: ['social'],
  data:()=>({
      form: {},
  }),

  methods: {
    send() {
      alert(JSON.stringify(this.form));

    },
  }
}
</script>
