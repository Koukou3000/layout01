<template>
    <div>
        <div class="header">面包屑 & 路由栈</div>

        <!-- 修改高度即可 -->
        <div class="body" style="height:calc(100vh - 400px)">
            <div class="panel">
                <div class="left">
                    <div class="a">
                        <div>
                            <br><br><br><br><br><br><br><br><br><br><br>
                            <br><br><br><br><br><br><br><br><br><br><br>
                        </div>
                    </div>
                
                    <div class="b">
                        <div>
                            <br><br><br><br><br><br><br><br><br><br><br>
                            <br><br><br><br><br><br><br><br><br><br><br>
                        </div>
                    </div>
                </div>
                <div class="right"></div>
            </div>
            
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header{
    text-align: center;
    padding: 10px;
    background: #fff;
    color: #000;
}


.body{
    height: calc(100vh - 100px);
    padding: 5px;
    background: red;
}
.panel{
    height: inherit;
    display: flex;
    gap: 10px;
}
.left{
    background: red;
    max-width: 250px;
    min-width: 250px;
    display: flex;
    flex-direction: column;
    gap: 10px;
}
.a{
    flex-basis: 1;
    flex-grow: 1;
    background: #888;
    overflow: scroll;
}
.b{
    flex-grow: 1;
    background: #888;
    overflow: scroll;
}


.right{
    background: #ccc;
    flex-grow: 1;
}




</style>