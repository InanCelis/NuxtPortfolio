<template>
  <div class="row ">
        <div v-for="(data, index) in work" :key="index" class="col-md-12 col-lg-6 col-sm-12 mb-4 d-flex w-100" >
            <i class="resume-icons fa fa-suitcase main-bg text-light m-0"></i>
            <p class="line"></p>
            <div class="col-10 border-left-2 shadow">
                <h6 class="mt-3 font-weight-bold dark-text" v-html="data.position"></h6>
                <div class="m-0 justify-content-between">
                  <div class="row m-0">
                    <a class="dark-text" v-html="data.company"></a>
                    <p v-html="' - '+data.type"></p>
                  </div>
                  <div class="row m-0">
                    <p class=" m-1 text-muted " v-html="data.dateFrom+ ' - '+ data.dateTo"></p>
                    <p class="text-muted m-1" v-html="'| '+ data.role"></p>
                  </div>
                </div>
                <div class="row m-0">
                    <p class="text-muted m-1" v-html="data.address"></p>
                </div>

                <hr class="bg-dark m-0">
                <div class="text-muted">
                    <p class="mt-2 m-1 mb-3 " v-html="data.description"></p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name:'Work',
  props: ['work'],
}
</script>
