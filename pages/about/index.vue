<template>
  <div>
    <PageName :page='"About"' :number='"02"' :other='"me"'/>
    <div class="row justify-content-center pb-5" >
        <figure class="col-md-4 m-0 text-center align-self-center">
            <img src="/images/ako.jpg" class="figure-img img-fluid" >
        </figure>
        <div class="col-md-7 border-main-left-4 mt-3" >
            <h3 class="mb-3 ml-3 font-weight-bold">Who Am I</h3>
            <h4 class="ml-3 font-weight-normal">I'm a web developer at Valens Research Asia.</h4>
            <div class="pl-3 text-muted">
                <p>
                  I enjoy problem solving and making websites such as landing pages, mock up design etc. A person who loves to learn a lot of things and sharing knowledge to others with the same field.
                </p>
                <table class="table table-borderless col-sm-12 col-md-8">
                    <tbody >
                        <tr v-for="(data, index) in users" :key="index">
                            <td class="text-muted font-weight-bold">{{ data.title }}</td>
                            <td>:</td>
                            <td class="dark-text">{{ data.content }}</td>
                        </tr>
                    </tbody>
                </table>
                <button @click="downloadPdf" class="btn btn-dark rounded-pill">Download CV</button>
            </div>
        </div>
    </div>
</div>
</template>

<script>

import axios from '@nuxtjs/axios';
export default {
  head() {
    return {
      title: 'About - Inan',
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
    url: 'http://localhost:3000/files/inan-resume.pdf',
    users: [
      {
        title: 'Name',
        content: 'Ferdinand Celis'
      },
      {
        title: 'Birthdate',
        content: 'September 4, 1998'
      },
      {
        title: 'Gender',
        content: 'Male'
      },
      {
        title: 'Address',
        content: 'Lilian st. Brgy. Bulihan Famy, Laguna'
      },
      {
        title: 'Email',
        content: 'celisinan@gmail.com'
      },
      {
        title: 'Contact',
        content: '+63926 8421 554'
      },
    ]
  }),

  methods: {
    downloadPdf() {
      this.$axios({
          url: 'http://localhost:3000/files/inan-resume.pdf',
          method: 'GET',
          responseType: 'blob',
      }).then((response) => {
            var fileURL = window.URL.createObjectURL(new Blob([response.data]));
            var fileLink = document.createElement('a');
            fileLink.href = fileURL;
            fileLink.setAttribute('download', 'inan-resume.pdf');
            document.body.appendChild(fileLink);
            fileLink.click();
      });

    },

  }

}
</script>
