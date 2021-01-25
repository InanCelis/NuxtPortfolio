<template>
  <div class="row ">
    <div v-for="(data, index) in education" :key="index" class="col-md-12 col-lg-6 col-sm-12 d-flex w-100 mb-4">
      <i class="resume-icons fa fa-graduation-cap main-bg text-light m-0"></i>
      <p class="line"></p>
      <div class="col-10 border-left-2 shadow">
            <h6 class="mt-3 font-weight-bold dark-text" v-html="data.qualification+ ' in ' + data.field"></h6>
            <p class="text-muted m-0" v-html="data.school"></p>
            <p class="text-muted m-0" v-html="data.address"></p>
            <p class="text-muted m-0 mb-3" v-html="data.from+ ' - ' + data.to"></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Education',
  props: ['education'],
}
</script>
