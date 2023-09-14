<template>
  <div class="app">

    <div class="left">左侧树</div>
    <div class="right">
      <div class="navbar">导航栏</div>
      <div class="main">
        <div class="wrapper">
          <div class="card">
            <div class="innerTop">
                  <el-table
                  :data="tableData"
                  height="100%">
                  <el-table-column
                  prop="date"
                  label="上">
                  </el-table-column>
                  </el-table>

            </div>
            <div class="innerBot">
                  <el-table
                  :data="tableData"
                  height="100%">
                  <el-table-column
                  prop="date"
                  label="下">
                  </el-table-column>
                  </el-table>

            </div>


          </div>
          <div class="card">
          vh继承下来的百分比（固定高度）+ flex-shrink
          </div>
          <div class="card">

          </div>
        </div>

      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'App',
  data(){
		return{
      tableData:[{date:1},
      {date:2},
      {date:3},
      {date:4},
      {date:5},
      {date:1},
      {date:2},
      {date:3},
      {date:4},
      {date:5},
      {date:1},
      {date:2},
			]
		}
	}
}
</script>

<style scoped>

  .app{
      color: white;
      margin: 0;
      height: 100vh;
      display: flex;
  }
  .left{
      width: 200px;
      background: skyblue;
  }
  .right{
      height: 100%;
      flex-grow: 1;
      display: flex;
      flex-direction: column;
  }
  .navbar{
      min-height: 100px;
      background: black;
  }
  .main{    
      height: calc(100% - 100px);
      flex-grow: 1;
      background-color: #ccc;
  }
  .wrapper{
      display: flex;
      box-sizing: border-box;
      background: #ccc;
      height: calc(100% - 16px);
      margin: 8px;
      gap: 8px;
  }
  .card{
      height: 100%;
      width: 100%;
      flex-grow: 1;
      background: #000;
      display: flex;
      flex-direction: column;
  }
  .innerTop{
    overflow: scroll;
    flex: 1 1 auto;
    background-color: aliceblue;
  }
  .innerBot{
    overflow: scroll;
    flex: 1 1 auto;
    background-color: palegoldenrod;
  }
</style>
