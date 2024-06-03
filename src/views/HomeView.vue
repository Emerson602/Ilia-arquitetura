<template>
  <div id="home">
    <ImageTransitionContainer />
  </div>
</template> 


<script>

import ImageTransitionContainer from '@/components/ImageTransitionContainer.vue'; 

  export default {
    name: 'HomeView',
    components: {
      ImageTransitionContainer,
    }
  }
</script>

<style scoped>
  div {
    width: 100%;
    height: 100vh;       
  }
</style>

