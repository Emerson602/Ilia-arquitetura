<template>
    <div id="transition-container" class="d-flex flex-column flex-lg-row col-12">
        <div id="images-transition" class="col-12 col-lg-6 d-flex justify-content-center align-items-start">           
            <img v-if="images[currentImage]" :src="require(`@/assets/${images[currentImage]}`)" :key="images[currentImage]" class="front col-12" />
            <img v-if="images[currentImage + 1]" :src="require(`@/assets/${images[currentImage + 1]}`)" :key="images[currentImage + 1]" class="back col-12 col-lg-6 position-absolute" /> 
             
        </div>
        <div class="col-12 col-lg-6 text-center">
            <h1 class="mt-5">Magda Emilia Arquitetura</h1>
            <p class="col-12 p-3 p-lg-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Error harum quidem optio aspernatur earum numquam soluta ad a
                 qui recusandae excepturi consequatur, necessitatibus esse fugit vero itaque ipsam dignissimos quasi.
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

