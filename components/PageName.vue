<template>
  <div class="row ml-2">
      <div class="h_line shadow" v-if="page"></div>
      <h5 class="text-center text-md-left text-uppercase font-weight-bold" v-html="page">
        <b class="main-text" v-if="other" v-html="other"></b>
      </h5>
    <span class="page-number d-none d-xl-block ml-auto" v-html="number"></span>
  </div>
</template>

<script>
export default {
  name: 'PageName',
  props:['page', 'number', 'other'],
}
</script>
