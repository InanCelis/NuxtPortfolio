<template>
  <div class="container">
    <div class="row ml-2">
        <span class="page-number dark-text d-none d-xl-block ml-auto">01</span>
    </div>
    <div class="row">
      <div class="col-lg-6 offset-lg-1">
        <img src="/images/me.png" class="my-image"/>
      </div>
      <div class="col-lg-5 banner-text">
        <h1 class="dark-text">Website</h1>
        <h2 class="dark-text">Developer</h2>
        <p class="text-muted">
          A website and front end developer who loves designing website and make the complex problem into simple.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Inan',
      meta: [
        {
          hid:'desccription',
          name: 'description',
          content: "Inans' Portfolio",
        }
      ]
    }
  },
}
</script>

