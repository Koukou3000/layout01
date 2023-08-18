<template>
  <div id="app">
    
    <innerModal/>
  
  </div>
</template>

<script>
import innerModal from './components/innerModal.vue'

export default {
  name: 'App',
  components: {
    innerModal
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
