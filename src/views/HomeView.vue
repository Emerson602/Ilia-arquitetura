<template>
  <div id="home">     
    <ImageTransitionContainer />
    <ApresentationContainer />
    <MostRecent />
    <Concept />
    <FollowMe />
    <Footer />
  </div>
</template> 


<script>

 
import ImageTransitionContainer from '@/components/ImageTransitionContainer.vue';
import ApresentationContainer from '@/components/ApresentationContainer.vue'; 
import MostRecent from '@/components/MostRecent.vue'; 
import Concept from '@/components/Concept.vue';
import FollowMe from '@/components/FollowMe.vue';

import Footer from '@/components/Footer.vue';

  export default {
    name: 'HomeView',
    components: {    
      ImageTransitionContainer,
      ApresentationContainer,
      MostRecent,      
      Concept, 
      FollowMe,  
      Footer,
    }
  }
</script>

<style scoped>
  div {
    width: 100%;
    height: 100vh;       
  }
  
</style>

