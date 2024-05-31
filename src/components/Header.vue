<template>
    <header id="header" class="d-flex justify-content-between align-items-center">
        <img class="m-3 mt-0 mb-0 m-lg-5 mt-lg-0 mb-lg-0" src="https://conteudo.imguol.com.br/c/entretenimento/e4/2021/12/03/pisco-o-gato-que-parece-o-gato-de-botas-do-shrek-2-1638547040040_v2_3x4.jpg">
        <div class="m-auto m-lg-5 mt-lg-0 mb-lg-0 bg-success position-lg-sticky">
            <Nav />                
        </div>
    </header>
</template>

  <script>

  import Nav from '@/components/Nav.vue'; 

  export default {
    name: 'Header', 
    components: {
      Nav, 
    }     
  }
  </script> 
  
<style scoped>

  #header {
    width: 100%;
    background-color: var(--pearl-bush);
  }

  #header img {
    width: 150px;
    height: auto;
  }
</style>
  
  