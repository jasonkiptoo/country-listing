<template>
  
  <Navbar/>
  <countryDisplay/>

</template>

<script>
import Navbar from './components/navBar.vue'
import countryDisplay from './components/countryDisplay.vue';

export default {
  name: 'App',
  components: {
    Navbar, countryDisplay
  }
}
</script>

<style>
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: right;
  color: #2c3e50;
  margin-top: 60px; */
}
</style>
