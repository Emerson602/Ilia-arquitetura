<template>
  <div class="about d-flex flex-column justify-content-center align-items-center mt-5 mb-5">
    <h2 class="fs-1 mt-5">Sobre mim</h2>

    <div class="d-flex flex-column flex-md-row justify-content-center align-items-center mt-5 mb-5">   

      <div class="col-12 col-md-6 mt-0 mt-md-5 d-flex justify-content-center align-items-center">
        <img :src="imgProfile" alt="Profile Image" class="col-10 col-md-8 rounded-circle">
      </div>
      
      <div class="col-12 col-md-6 mt-5 m-md-0 d-flex justify-content-center align-items-center">
        <p class="col-10 fs-5">
          Magda Nascimento - Arquiteta e Urbanista
          Formada pela Universidade Federal de Alagoas, Magda Nascimento é uma arquiteta e urbanista apaixonada por criar espaços que equilibrem funcionalidade, estética e sustentabilidade. Com uma visão inovadora, seu trabalho valoriza o uso de materiais naturais, como madeira e pedra, integrando-os de maneira harmoniosa ao design de interiores. Magda busca sempre soluções que respeitem o meio ambiente, criando ambientes acolhedores e únicos.
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
        imgProfile: require('@/assets/profile-image.webp'),
      }
    },
  }
</script>

