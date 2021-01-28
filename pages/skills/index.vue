<template>
  <div>
      <PageName :page='"Skills"' :number='"04"'/>
      <div class="pb-5">
          <h4 class="font-weight-bold mb-4">Skills & endorsements</h4>
          <div class="row m-0">
            <div v-for="(data, index) in skills.top" :key="index" class="col-md-12 mb-3">
                <b class="align-self-center text-capitalize" v-html="data.name"></b>
                <hr class="dark-bg">
            </div>
          </div>

          <h5 class="text-muted mb-4">Tools & Technologies </h5>
          <div class="row m-0">
            <div v-for="(data, index) in skills.tools" :key="index" class="col-6 mb-3">
                <div class="row content m-0">
                  <img v-if="data.image" :src="'/images/skills/'+data.image">
                  <b class="align-self-center text-capitalize" v-html="data.name"></b>
                </div>
            </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Skills - Inan',
      meta: [
        {
          hid:'desccription',
          name: 'description',
          content: "Inans' Portfolio",
        }
      ]
    }
  },
  data:()=>({
    skills :
      {
        top: [
          { type: 1, name: 'Web Development' },
          { type: 1, name: 'Web Design' },
          { type: 1, name: 'Responsive Web Design' },
        ],
        tools: [
          { name: 'Laravel', image: 'lara.png' },
          { name: 'PHP', image: 'php.png' },
          { name: 'MySql', image: 'mysql.png' },
          { name: 'CSS', image: 'css.png' },
          { name: 'Bootstrap', image: 'bootstrap.png' },
          { name: 'HTML', image: 'html.png' },
          { name: 'SASS', image: 'sass.png' },
          { name: 'JavaScript', image: 'javascript1.png' },
          { name: 'AJAX', image: 'ajax.png' },
          { name: 'jQuery', image: 'jquery.png' },
          { name: 'VueJs', image: 'vue.png' },
          { name: 'C#', image: 'csharp.png' },
          { name: 'Photoshop', image: 'pshop.png' },
          { name: 'Adobe XD', image: 'xd.png' },
        ]
      },
  }),
}
</script>

<style lang="scss" scoped>
.content {
  gap: 0.7em;
  img {
    width: 40px;
  }
}

</style>
