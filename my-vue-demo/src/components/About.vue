<template>
  <div>
      <h1>{{title}}</h1>
      <div id="about_2">
          <span>name:</span>
          <el-input size="mini" v-model="aboutName" placeholder="点击按钮显示名字"></el-input>
          <el-button type="info" size="mini" @click="showName">按钮</el-button>
      </div>
  </div>
</template>

<script>
export default {
    name:'About',
    props:{
        title:String
    },
    data(){
        return{
            aboutName:""
        }
    },
    methods:{
        showName:function(){
            this.aboutName='赵鹏飞'
        }
    }
}
</script>

<style scoped>
    /* #about_2{
        height: 15px
    } */
    .el-input{
        width: 300px;
        margin: 0 5px;
    }
    span{
        font-size: 30px;
    }
</style>