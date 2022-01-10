<template>
 <div>
     <b-navbar>
        <template #brand>
            <b-navbar-item tag="router-link" :to="{ path: '/' }">
                <img
                    src="../assets/logo1.png"
                    
                >
            </b-navbar-item>
        </template>
        <template #start>
            <b-navbar-item  >
               <router-link :to="{name: 'home' }">Home</router-link>
            </b-navbar-item>
            <b-navbar-item >
                <router-link :to="{name: 'about' }">About</router-link>
            </b-navbar-item>
            
                <b-navbar-item >
                    <router-link :to="{name: 'contact' }">Contact</router-link>
                </b-navbar-item>
                <b-navbar-item >
                   <router-link :to="{name: 'projects' }">All Projects</router-link>
                </b-navbar-item>
           
        </template>

        <template #end>
            <b-navbar-item tag="div">
                <div class="buttons">
                    <a class="button is-primary">
                        <strong>Sign up</strong>
                    </a>
                    <a class="button is-light">
                        Log in
                    </a>
                </div>
            </b-navbar-item>
        </template>
    </b-navbar>
    
  
</div>
</template>

<script>

export default {
  name: 'Navbar',
  components: {
    
  }
}
</script>

<style>


</style>