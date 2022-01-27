//App.vue
<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
        <Navbar/>
        </div>
        </div>
    </div>
    <div class="container pt-4">
      <div class="row">
      </div>
      <router-view/>
    </div>
    <nav class="">
      <img alt="Vue Footer" src="./assets/Footer.png" style="widht:100%">
    </nav>
  </div>
</template>
<script> 
  import Navbar from '@/components/Navbar.vue'
  
  export default { 
    components: {
      Navbar
    }
  }
</script>
<style>
  #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; 
  color: #2c3e50;
  } 
  #app .navbar-nav a{ 
  color: #2c3e50;
  cursor: pointer;
  }
  #app .navbar-nav a.router-link-exact-active {
  color: #42b983;
  }
</style>

