<template>
  <div id="app">

    <el-container class="big">
      <el-header>
        <h1>VUE DAMO</h1>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <el-menu
            default-active="2"
            class="el-menu-vertical-demo"
            >
            <router-link to="/">
              <el-menu-item index="1">
                <i class="el-icon-s-home"></i>
                <span slot="title">Home</span>
              </el-menu-item>
            </router-link>
            <el-submenu index="2">
              <template slot="title">
                <i class="el-icon-s-order"></i>
                <span>作业列表</span>
              </template>
              <el-menu-item-group>
                <router-link to="/about"><el-menu-item index="2-1">About</el-menu-item></router-link>
                <el-menu-item index="2-2" disabled>选项2</el-menu-item>
              </el-menu-item-group>
            </el-submenu>
            <el-menu-item index="3">
              <i class="el-icon-menu"></i>
              <span slot="title">其它</span>
            </el-menu-item>
          </el-menu>
          <!-- <ul>
            <router-link to="/"><li>Home</li></router-link>
            <router-link to="/about"><li>About</li></router-link>
          </ul> -->
        </el-aside>
        <el-main>
          <router-view/>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>


<style scoped>
  .big{
    min-height: 100vh;
  }

  .el-header{
      background-color: #B3C0D1;
      text-align: center;
      line-height: 50px;
    }
  
  .el-aside {
    background-color: #D3DCE6;
    text-align: center;
  }
  a{
    text-decoration: none;
  }
  /* .el-main {
    background-color: #E9EEF3;
  } */
</style>
