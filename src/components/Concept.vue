<template>
    <section id="concept" class="pt-5 pb-5 col-12 d-flex flex-column flex-lg-row justify-content-center align-items-center">

        <div class="p-5 col-12 col-lg-5">
           <h2 class="fs-1">lorem ipsum</h2>
           <p class="fs-5 mt-5">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit.
            Labore tempora quam fugiat doloremque impedit. Nemo ipsa 
            cumque quam, debitis est totam temporibus minima nulla!
            Odio a impedit ipsa unde ullam!
           </p>
        </div>
        
        <img class="col-10 col-lg-4" :src="image" alt=""/>
        
    </section>
</template>

<script>
export default {
  name: 'Concept',
  data() {
    return {
        image: require('@/assets/4.webp')
    };
  },
  methods: {
   
  },
  mounted() {
  
  }
}
</script>

<style scoped>
#concept {
    background-color: var(--natural);     
} 
</style>
