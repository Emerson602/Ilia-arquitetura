<template>
  <div class="about d-flex flex-column justify-content-center align-items-center mt-5 mb-5">
    <h2 class="fs-1 mt-5">Sobre mim</h2>

    <div class="d-flex flex-column flex-md-row justify-content-center align-items-center mt-5 mb-5">   

      <div class="col-12 col-md-6 mt-0 mt-md-5 d-flex justify-content-center align-items-center">
        <img :src="imgProfile" alt="Profile Image" class="col-10 col-md-8">
      </div>
      
      <div class="col-12 col-md-6 mt-5 m-md-0 d-flex justify-content-center align-items-center">
        <p class="col-10 fs-5">
          Lorem ipsum dolor sit amet consectetur,
          adipisicing elit. Ipsum obcaecati quia 
          aperiam repellat sint voluptas adipisci
          facere et? Quidem molestiae eveniet eius
          assumenda a sapiente aut incidunt qui
          doloribus ipsam?
        </p>
      </div>

    </div> 
  </div>
  <Footer />
</template>

<script>
  import Footer from '@/components/Footer.vue';

  export default {
    name: 'AboutView',
    components: {
      Footer
    },
    data() {
    return {
      imgProfile: require('@/assets/3.webp'),
    }
  },
  }
</script>

<style scoped>

</style>

