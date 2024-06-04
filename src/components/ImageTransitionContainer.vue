<template>
    <div id="transition-container" class="h-auto d-flex flex-column flex-lg-row col-12">
        <div id="images-transition" class="col-12 col-lg-6 d-flex justify-content-center align-items-start">           
            <img class="front col-12" v-if="images[currentImage]" :src="require(`@/assets/${images[currentImage]}`)" :key="images[currentImage]" alt="image-banner"/>
            <img class="back col-12 col-lg-6 position-absolute" v-if="images[currentImage + 1]" :src="require(`@/assets/${images[currentImage + 1]}`)" :key="images[currentImage + 1]" alt="image-banner"/>               
        </div>
        <div class="col-12 col-lg-6 text-center p-2 pt-5 pb-5 p-lg-5">
            <h1 class="mt-lg-5  fs-1">Magda Emilia Arquitetura</h1>
            <p class="mt-4 mt-lg-5 col-12 fs-2 text-center text-lg-start">
                Construindo espaços que respiram vida e inspiração.
            </p>
        </div>
    </div>
</template>
    
<script>
export default {
    name: 'ImageTransitionContainer', 
    data() {
      return {
        currentImage: 0,        
        images: [
        '1.webp',
        '2.webp',
        '3.webp',
        ],
      }   
    },
    methods: {
        imageTransition() {
            
            this.currentImage++                   

            if(this.currentImage > 2) {
                this.currentImage = 0
            }            
        }
    },
    mounted() {
       
       const transitionInterval = setInterval(() => {
          this.imageTransition();
        }, 15000)
    }
}
</script>   
    
<style scoped>     
    #images-transition {
        overflow: hidden;
    }

    .front {
        animation: front 10s  ease-in;
        animation-delay: 5s;
        opacity: 1;
        transition: 3s;
    
    }

    @keyframes front {
        0% {
           opacity: 1;          
        }

    
       100% {
           opacity: 0;        
        }
    }

    .back {
        animation: back 10s  ease-in;
        animation-delay: 5s;
        opacity: 0;
        transition: 3s;
     
    }

    @keyframes back {
        0% {
           opacity: 0;
  
        }

       100% {
           opacity: 1; 
        }
    }

  
</style>

