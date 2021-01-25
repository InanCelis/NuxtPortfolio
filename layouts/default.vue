<template>
  <div>
    <SocialIcon :social="socials"/>
    <Header />
    <Nuxt class="container page-content"/>
    <Foot :social="socials"/>
  </div>
</template>
<script>
import Header from '../components/Header';

export default {
  components: {
    Header,
  },
  data:()=>({
    socials: [
      {
        url: 'https://www.facebook.com/INAN.454/',
        name: 'Facebook',
        icon: 'fa-facebook-f',
      },
      {
        url: 'https://www.instagram.com/inan0_4/',
        name: 'Instagram',
        icon: 'fa-instagram',
      },
      {
        url: 'https://www.linkedin.com/in/ferdinand-celis-099394172/',
        name: 'LinkedIn',
        icon: 'fa-linkedin-in',
      },
      {
        url: 'https://github.com/InanCelis',
        name: 'Github',
        icon: 'fa-github',
      },
    ]
  }),
}
</script>
<style>

</style>
