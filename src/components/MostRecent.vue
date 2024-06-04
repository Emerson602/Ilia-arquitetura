<template>
    <section id="most-recent" class="col-12 pt-5 pb-5 d-flex flex-row justify-content-center align-items-center flex-wrap"> 

        <div id="container-overlay" class="position-relative col-10 col-sm-7 col-md-5 col-lg-3 m-4 d-flex justify-content-center align-items-center">
            <div id="overlay" class="p-2 position-absolute d-flex flex-column justify-content-center align-items-center col-10 col-sm-7 col-md-5 col-lg-3">
                <span>lorem ipsum</span>
            </div>
            <img class="col-12" src="../assets/1.webp">
        </div>

        <div id="container-overlay" class="position-relative col-10 col-sm-7 col-md-5 col-lg-3 m-4 d-flex justify-content-center align-items-center">
            <div id="overlay" class="p-2 position-absolute d-flex flex-column justify-content-center align-items-center col-10 col-sm-7 col-md-5 col-lg-3">
                <span>lorem ipsum</span>
            </div>
            <img class="col-12" src="../assets/2.webp">
        </div>

        <div id="container-overlay" class="position-relative col-10 col-sm-7 col-md-5 col-lg-3 m-4 d-flex justify-content-center align-items-center">
            <div id="overlay" class="p-2 position-absolute d-flex flex-column justify-content-center align-items-center col-10 col-sm-7 col-md-5 col-lg-3">
                <span>lorem ipsum</span>
            </div>
            <img class="col-12" src="../assets/3.webp">
        </div>       
 
    </section>  
</template>
    
<script>
export default {
    name: 'MostRecent', 
    data() {
      return {
       
      }   
    },
    methods: {
      
    },
    mounted() {
    
    }
}
</script>   
    
<style scoped>     
    #most-recent {
        background-color: var(--pearl-bush);
    }

    #overlay {     
        height: 100%;
        width: 100%;
        opacity: 0;
        transition: 1s ease-in;
        background-color: var(--cocoa);
    }

    #container-overlay img {
        display: block;
        width: 100%;
        height: auto;  
    }

    #most-recent div:hover, #content:hover {
        opacity: 1;  
    } 

    #container-overlay:hover #overlay {
        opacity: 1;
    }  

</style>

