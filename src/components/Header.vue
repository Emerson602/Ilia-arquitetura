<template>
    <header id="header" class="d-flex justify-content-between align-items-center">         
        <img class="m-3 mt-0 mb-0 m-lg-5 mt-lg-0 mb-lg-0" src="https://conteudo.imguol.com.br/c/entretenimento/e4/2021/12/03/pisco-o-gato-que-parece-o-gato-de-botas-do-shrek-2-1638547040040_v2_3x4.jpg">
        <svg @click="toggleMenu" id="close" v-if="showClose" xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-x-lg d-lg-none m-3" viewBox="0 0 16 16">
            <path d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"/>
        </svg>
        <svg @click="toggleMenu" id="bar" v-if="showBar" xmlns="http://www.w3.org/2000/svg" width="45" height="45" fill="currentColor" class="bi bi-list d-lg-none m-3" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5"/>
        </svg>
        <div id="menu-mobile" v-if="showNav" class="d-flex justify-content-center align-items-center text-center m-lg-5 mt-lg-0 mb-lg-0"> 
           <Nav />                
        </div>
        <div id="menu-desktop" class="d-none d-lg-flex justify-content-center align-items-center text-center m-lg-5 mt-lg-0 mb-lg-0"> 
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
    },
    data() {
      return {
        showNav: false,
        showBar: true,
        showClose: false,
      }   
    },
    methods: {
    toggleMenu() {      
      this.showNav = !this.showNav;
      this.toggleIcon();
    },
    toggleIcon() {
      this.showBar = !this.showBar;
      this.showClose = !this.showClose;
    },
    checkScreenSize() {        
        const screenWidth = window.innerWidth;    
               
        if (screenWidth >= 992) {             
            this.toggleMenu();
        }
    }, 
    },
    mounted() {
    
    } 
    
  } 
  </script> 
  
<style scoped> 

  #header {
    width: 100%;
    background-color: var(--pearl-bush);
  }

  #header img {
    width: 100px;
    height: 100px;
  }  

</style>
  
  