<template>
  <section class="col-12 pt-5 pb-5 d-flex flex-column justify-content-center align-items-center">
    <div id="gallery-container" class="d-flex flex-row justify-content-center align-items-center flex-wrap">
      <div id="project" class="col-4 m-3 d-flex flex-column justify-content-center align-items-center" v-for="(project, index) in visibleProjects" :key="index">
        <h3>{{ project.name }}</h3>
        <p>{{ project.description }}</p> 
        <img class="col-12" :src="project.images[0]" alt="Project Image">       
      </div>      
    </div>
    <button id="show-more" @click="showMoreProjects">
        <svg v-if="maxProjects <= totalProjects" xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-chevron-double-down" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M1.646 6.646a.5.5 0 0 1 .708 0L8 12.293l5.646-5.647a.5.5 0 0 1 .708.708l-6 6a.5.5 0 0 1-.708 0l-6-6a.5.5 0 0 1 0-.708"/>
          <path fill-rule="evenodd" d="M1.646 2.646a.5.5 0 0 1 .708 0L8 8.293l5.646-5.647a.5.5 0 0 1 .708.708l-6 6a.5.5 0 0 1-.708 0l-6-6a.5.5 0 0 1 0-.708"/>
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-chevron-double-up" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M7.646 2.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1-.708.708L8 3.707 2.354 9.354a.5.5 0 1 1-.708-.708z"/>
          <path fill-rule="evenodd" d="M7.646 6.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1-.708.708L8 7.707l-5.646 5.647a.5.5 0 0 1-.708-.708z"/>
        </svg>
      </button>
      <ProjectModal />
  </section>

</template>


<script>
import ProjectModal from '@/components/ProjectModal.vue'; 
export default {
  name: 'Gallery',
  components: {
    ProjectModal,     
  },
  data() {
    return {
      projects: [],
      totalProjects: 0,
      maxProjects: 4,
      showMore: true,
    }
  },
  computed: {
    visibleProjects() {
      return this.projects.slice(0, this.maxProjects);
    }
  },
  methods: {
    createProjects() {
      const projects = [
        {
          name: 'project 1',
          description: 'lorem ipsum',
          images: [require('@/assets/1.webp'), require('@/assets/2.webp'), require('@/assets/3.webp')]
        },
        {
          name: 'project 2',
          description: 'lorem ipsum',
          images: [require('@/assets/2.webp'), require('@/assets/1.webp'), require('@/assets/3.webp')]
        },
        {
          name: 'project 3',
          description: 'lorem ipsum',
          images: [require('@/assets/3.webp'), require('@/assets/1.webp'), require('@/assets/2.webp')]
        },
        {
          name: 'project 4',
          description: 'lorem ipsum',
          images: [require('@/assets/3.webp'), require('@/assets/1.webp'), require('@/assets/2.webp')]
        },
      ];
      
      this.totalProjects = projects.length;
      this.projects = projects;
    },
    showMoreProjects() {
      const numberVisibleProjects = 4;

      if (this.maxProjects < this.totalProjects) {
        this.maxProjects += numberVisibleProjects;
      } else {
        this.maxProjects = numberVisibleProjects;
      }
    },
  },
  mounted() {
    this.createProjects();   
  }
}
</script>
<style scoped>
#gallery-container {
  padding: 20px;
}

#project img {
  max-width: 100%;
  height: auto;
}

#show-more {
  background: none;
  border: none;
  cursor: pointer;
  margin-top: 20px;
}

button { 
  background-color: var(--cocoa) !important; 
  padding: 10px 80px;
  border-radius: 10px; 
}

svg {
  fill: #fff;
}
</style>
