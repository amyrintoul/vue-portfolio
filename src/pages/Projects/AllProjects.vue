<template>
<div>
   <h1 class=" text-uppercase font-weight-bold title is-1">All Projects</h1>
  <b-field label="Search Projects ">
            <b-input type="text" v-model="searchTerm" />
            
         </b-field>        
  

 <div class="row mb-5 justify-content-center">
      <div class="col-4">

         
         
        <!--<button @click="searchProjects()">Search</button>-->
  
         <div class="card"
            v-for="project in filteredProjects"
            :key="project.id"
         >
          
          
  <div class="card-image">
    <figure class="image is-4by3">
      
      <img :src="('@/assets/images/' + project.images)" alt="Placeholder image">
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
      <div class="media-content">
        <p class="title is-4">{{project.title}}</p>
        <p class="subtitle is-6">Created By Amy Rintoul</p>
        <b-taglist>
            <b-tag
            v-for="tag in project.tags"
            :key="tag"
            type="is-primary"
            >
            {{tag}}
            </b-tag>
        </b-taglist>
      </div>
    </div>
    <div class="content">
       {{project.description}}
      <br>       
      <a href="#">#css</a> <a href="#">#responsive</a>
      <br>
      <time datetime="2016-1-1" >{{project.date}}</time>
      <br>
      <div class="mt-2"></div>
      <b-button class="mr-2" v-if="project.demo" :to="{name: project.demo}" type="is-primary">Demo</b-button>
      
       <b-button class="mr-2" v-if="project.links.github" :href="project.links.github" type="is-primary">Github </b-button>
        <b-button class="mr-2" v-if="project.website" :href="project.website" type="is-primary">Hosted Site </b-button>

    
     
    </div>
  </div>
</div>
     </div>







     
 </div>
</div>
</template>

<script>


export default {
  name: 'AllProjects',
  components: {
    
  },
  data(){
      return{
          projects: [],
          searchTerm: ""
      }
  },
  computed:{
      filteredProjects: function () {
        return this.projects.filter(project => {
            return project.title.toLowerCase().includes(this.searchTerm.toLowerCase()) //includes can only be implied to a string
        })
      }
  },
  mounted(){
      this.getAllProjects()
  },
  methods:{
      getAllProjects(){
          fetch('./data/projects.json')
          .then(res => res.json())
          .then(data => {
              console.log(data)
              this.projects = data
          
        })


    },
    searchProjects(){
        

    },
    

  }
  
}
</script>

<style>

 
</style>