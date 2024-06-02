<template> 
  <Header />
  <router-view/>
</template>

<script>

  import Header from '@/components/Header.vue';

  export default {
    name: 'App',
    components: {
      Header,
    },

  }
</script>

<style>
 * {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Raleway", sans-serif;  
  color: #000;   
 }

 :root {
  --pearl-bush: #E3DED1;
  --bison-hide: #C1B59F;
  --stonewall: #908471;
  --soya-bean: #5F5A4D;
  --pale-oyster: #969286;
  --armadillo: #4F493F;
  --pale-brown: #908161;
  --old-copper: #786037;
  --organio: #646F40;
  --butter: #CBB89D;
  --coconut: #EDE1D2;
  --natural: #806044;
  --palm-oil: #502510;
  --cocoa: #412F26;
}

#nav ul, #nav a {
    text-decoration: none;
    list-style: none; 
}

li:hover, a:hover {
  color: var(--coconut);
  transition: 1s;
}

@media(max-width: 992px) { 

  #menu-mobile {    
      overflow-y: hidden;     
      background-color: var(--cocoa);        
      animation: nav-animation 0.5s ease-in; 
      animation-delay: 0s;          
      animation-fill-mode: forwards; 
      height: 60px;
      width: 10px;
      position: fixed;      
      right: 0;
      top: 0; 
      z-index: 99; 
      margin: 40px;  
      font-size: 0rem;
      rotate: -90deg;   
      opacity: 0;                          
    }
  } 

  #close {   
    z-index: 100;   
  } 

  @keyframes nav-animation {
      0% {
        rotate: -90deg;
        opacity: 0;
      }  
      25%{
        height: 60px;
        width: 10px;
        position: fixed;         
        right: 0;
        top: 0; 
        z-index: 99; 
        margin: 40px;  
        font-size: 0rem;
        rotate: -0deg;   
        opacity: 1;       
      }
      100% {
        height: 100%;
        width: 100%;
        position: fixed;         
        right: 0;
        top: 0;          
        margin: 0;  
        font-size: 1.4rem;  
        rotate: -0deg; 
        opacity: 1;
      }
  }



  


</style>
