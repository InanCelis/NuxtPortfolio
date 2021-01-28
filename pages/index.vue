<template>
  <div>
    <PageName :number='"01"'/>
    <div class="row">
      <div class="col-lg-6 offset-lg-1">
        <img src="/images/me.png" class="my-image"/>
      </div>
      <div class="col-lg-5 banner-text">
        <h1>Website</h1>
        <h2>Developer</h2>
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

