<template>
  <div class="container">
      <div class="row ml-2">
          <div class="h_line shadow"></div>
          <h5 class="text-center text-md-left text-uppercase font-weight-bold dark-text" >Resumes</h5>
          <span class="page-number dark-text d-none d-xl-block ml-auto">03</span>
      </div>
      <div class="row d-flex pb-5" >
          <div class="container">
              <div class="row">
                  <div class="col-md-12 mb-4" v-if="works.length">
                      <h4 class="font-weight-bold mb-4 dark-text">Working Experience</h4>
                      <!-- this is from component resume no need to import it still work -->
                      <Work :work="works"/>
                  </div>
                  <div class="col-md-12 mb-4" v-if="educations.length">
                      <h4 class="font-weight-bold mb-4 dark-text">Educational Background</h4>
                      <!-- this is from component resume no need to import it still work -->
                      <Education :education="educations"/>
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
      title: 'Resume - Inan',
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
    works: [
      {
        position: 'Web Developer',
        dateFrom: 'Jan 2020',
        dateTo: 'Present',
        role: 'Front end Developer',
        company: 'Valens Research Asia',
        type: 'Full-time',
        address: 'Pasig, National Capital Region, Philippines',
        description: 'Lorem ipsum dolor sit amet co amet consectetur adipisicing elit. Deserunt sit nihil rem porro ipsam cum, sunt repudiandae, reprehenderit placeat quas voluptatem sed culpa harum. Alias atque nostrum iusto sed aperiam? unde.'
      },
      {
        position: 'Web Developer',
        dateFrom: 'Aug 2019',
        dateTo: 'Jan 2020',
        role: 'Fullstack Developer',
        company: 'Youth Development Affairs of Laguna',
        type: 'Internship',
        address: 'Santa Cruz, Laguna',
        description: 'Lorem ipsum dolor sit amet co amet consectetur adipisicing elit. Deserunt sit nihil rem porro ipsam cum',
      }
    ],

    educations: [
      {
        qualification: "Bachelor's/College Degree",
        field: 'Information Technology',
        school: 'Laguna State Polytechnic University',
        address:'Santa Cruz, Laguna Philippines',
        from: '2017',
        to: '2020',
      },
      {
        qualification: "Bachelor's/College Degree",
        field: 'Computer Science',
        school: 'Colegion De San Lorenzo',
        address:'Congressional Ave, Project 8, Quezon City, Metro Manila Philippines',
        from: '2015',
        to: '2017',
      }
    ]
  }),
}
</script>
