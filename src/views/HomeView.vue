<template>
  <div id="home">     
    <ImageTransitionContainer />
    <MostRecent />
  </div>
</template> 


<script>

 
import ImageTransitionContainer from '@/components/ImageTransitionContainer.vue'; 
import MostRecent from '@/components/MostRecent.vue'; 

  export default {
    name: 'HomeView',
    components: {    
      ImageTransitionContainer,
      MostRecent,
    }
  }
</script>

<style scoped>
  div {
    width: 100%;
    height: 100vh;       
  }
  
</style>

