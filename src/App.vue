<template>
  <div id="app">
    <!-- 1.提示框吸附 -->
    <div style="height:100px;overflow:hidden;">
      <innerModal/>
    </div>

    <!-- 2.路由列表对齐 -->
    <adjustList/>
    
  </div>
</template>

<script>
import adjustList from './components/adjustList.vue'
import innerModal from './components/innerModal.vue'


export default {
  name: 'App',
  components: {
    innerModal,
    adjustList
  }
}
</script>

<style>
body{
  margin: 0 auto;
  background: #000;
}
</style>
