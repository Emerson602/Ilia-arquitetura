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
    }
  }
</script>

<style>
 * {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
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

</style>
