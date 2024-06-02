<template>
  <nav id="nav">
    <ul class="d-flex flex-column flex-lg-row justify-content-lg-center align-items-lg-center m-0 p-0 text-uppercase">
      <router-link to="/"><li class="m-2 m-lg-2">Inicio</li></router-link> 
      <router-link to="/projects"><li class="m-2 m-lg-2">Projetos</li></router-link> 
      <router-link to="/about"><li class="m-2 m-lg-2">Sobre</li></router-link>
      <a class="m-2 m-lg-2" href="https://api.whatsapp.com/send?phone=5582993975054" target="_blank"><li>Quero um projeto</li></a>
    </ul>            
  </nav>  
</template>
  
  <script>
  export default {
    name: 'NavDesktop', 
  }
  </script>   
   
  <style scoped> 


    

  </style>
  