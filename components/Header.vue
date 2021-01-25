<template>
    <b-navbar toggleable="lg" class="fixed-top light-bg" id="navbar">
      <div class="container">
        <b-navbar-brand :to="{ name:'index' }" class="logo-name dark-text">inan</b-navbar-brand>
        <div class="toggle-btn" id="_1st-toggle-btn">
          <input type="checkbox" @change="toggleTheme" >
          <span></span>
        </div>
        <b-navbar-toggle target="nav-collapse" class="icon"><i class="fas fa-bars dark-text "></i></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto ml-sm-center">
              <li class="nav-item">
                <nuxt-link :to="{ name:'about'} " class="nav-link">About</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link :to="{ name:'resume'} " class="nav-link">Resume</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link :to="{ name:'skills'} " class="nav-link">Skills</nuxt-link>
              </li>
              <!-- <li class="nav-item">
                <nuxt-link :to="{ name:'skills'} " class="nav-link">Skills</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link :to="{ name:'portfolio'} " class="nav-link">Portfolio</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link :to="{ name:'blog'} " class="nav-link">Blog</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link :to="{ name:'contact'} " class="nav-link">Contact</nuxt-link>
              </li> -->
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
</template>
<script>
export default {
  name: "Header",
  data() {
      return {
          theme: '' //When this property is empty, the theme is set to the default theme i.e. light mode.
      };
  },
  mounted() {
      let localTheme = localStorage.getItem('theme'); //gets stored theme value if any
      document.documentElement.setAttribute('data-theme', localTheme); // updates the data-theme attribute
  },

  methods: {
    toggleTheme() {
      this.theme = this.theme == 'darkMode' ? '' : 'darkMode'; //toggles theme value
      document.documentElement.setAttribute('data-theme', this.theme); // updates the data-theme attribute
      localStorage.setItem('theme', this.theme); // stores theme value in local storage
    }
  }
}
</script>
