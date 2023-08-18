<template>
  <div class="modal-content frame" ref="frame">

    <div class="panel top" ref="ctrl">
      <el-button type="primary">主要按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
    </div>

    <div class="panel mid" ref="mid" :style="{height: midHeight+'px'}">
      <div class="panel left">
            <el-table :data="tableData" >
                <el-table-column prop="item" label="试验项目"/>
            </el-table>
      </div>
      <div class="panel right">
        <el-tabs v-model="activeName" @tab-click="handleClick">
          <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
          <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
          <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
          <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
        </el-tabs>
         frame高度{{frameHeight}}
          <pre>
            1  
              2
                3
                  4
                    5
                      6
                        7 
                          8
                            9
                              10
          </pre>
      </div>
    </div>


    <div class="bot" ref="hint">
      [提示]
    </div>

  </div>
</template>

<script>
export default {
  data(){
    return{
      tableData:[{item:1},
                  {item:'2'},
                  {item:'3'},
                  {item:'4'},
                  {item:'5'},
                  {item:'2'},
               ],
      
      frameHeight: 0,
      ctrlHeight: 0,
      hintHeight: 0
    }
  },
  computed:{
    midHeight(){
      return this.frameHeight - this.ctrlHeight - this.hintHeight 
    }
  },
  mounted(){
    this.frameHeight = this.$refs.frame.getBoundingClientRect().height
    this.ctrlHeight = this.$refs.ctrl.getBoundingClientRect().height
    this.hintHeight = this.$refs.hint.getBoundingClientRect().height
    console.log(this.frameHeight, this.ctrlHeight, this.hintHeight)
    window.onresize = ()=>{
      this.frameHeight = this.$refs.frame.getBoundingClientRect().height
    }
  },
}
</script>



<style scoped>
.frame{
  position: relative;
  margin: 0 auto;
  height: calc(100vh - 200px);
  overflow: hidden;
}

.modal-content{
  position: relative;
  border: 1px solid black;
  display: flex;
  background-color: rgb(245,245,245);
  flex-direction: column;
}
.panel{
  box-sizing: border-box;
  border-radius: 4px;
  padding: 5px;
  background: #fff;
}
.top{
  display: flex;
  justify-content: left;
}
.mid{
  display: flex;
  flex-direction: row;
  background: rgb(245,245,245);
  overflow: hidden;
}
.left{
  flex-grow: 0;
  overflow-y: scroll;
  min-width: 150px;
  margin-bottom: 5px;
}
.right{
  flex-grow: 1;
  overflow-y: scroll;
  margin-bottom: 5px;
}

.bot{
  text-align: start;
  color: red;
  padding-left: 5px;
  line-height: 40px;
  background: #fff;
  position: absolute;
  bottom: 0;
  width: 100%;
}
</style>
