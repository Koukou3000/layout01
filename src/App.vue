<template>
  <div id="app">
    <!-- 1.提示框吸附 -->
    <!-- <div style="height:100px;overflow:hidden;">
      <innerModal/>
    </div> -->
    
    <!-- 2.对齐，单页问题 -->
    <pageSolution/>
  </div>
</template>

<script>
// import innerModal from './components/innerModal.vue'
import pageSolution from './components/pageSolution.vue'

export default {
  name: 'App',
  components: {
    // innerModal,
    pageSolution
  },
}
</script>

<style>
</style>