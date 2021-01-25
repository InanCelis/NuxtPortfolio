<template>
  <div class="container">
    <div class="row ml-2">
        <div class="h_line shadow"></div>
        <h5 class="text-center text-md-left text-uppercase font-weight-bold dark-text" >About
        <b class="main-text">Me</b>
      </h5>
        <span class="page-number dark-text d-none d-xl-block ml-auto">02</span>
    </div>
    <div class="row justify-content-center pb-5" >
        <figure class="col-md-4 m-0 text-center align-self-center">
            <img src="/images/ako.jpg" class="figure-img img-fluid" >
        </figure>
        <div class="col-md-7 border-main-left-4 mt-3" >
            <h3 class="mb-3 ml-3 font-weight-bold dark-text">Who Am I</h3>
            <h4 class="ml-3 font-weight-normal dark-text">I'm a web developer at Valens Research Asia.</h4>
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
                <a class="btn btn-dark rounded-pill">Download CV</a>
            </div>
        </div>
    </div>
</div>
</template>

<script>
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

}
</script>
