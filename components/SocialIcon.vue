<template>
  <div class="d-none d-md-block">
    <div class="icons">
      <a v-for="(data, index) in social" :key="index" :href="data.url" target="__blank">
        {{ data.name }} <i :class="'fab '+ data.icon"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SocialIcon',
  props: ['social'],
}
</script>
