<template>
  <div id="app">
    <el-calendar v-model="value"></el-calendar>

    <el-card class="box-card">
      <div v-for="size in sizeList" :key="size" class="text item">
        <transition name="el-fade-in-linear">
          <el-row :gutter="20">
            <el-col :span="6"><div class="grid-content bg-purple"><el-avatar shape="circleUrl" :size="size" :src="circleUrl"></el-avatar></div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple"><el-avatar shape="square" :size="size" :src="squareUrl"></el-avatar></div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple"><el-avatar shape="circleUrl" :size="size" :src="circleUrl"></el-avatar></div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple"><el-avatar shape="square" :size="size" :src="squareUrl"></el-avatar></div></el-col>
          </el-row>
        </transition>
      </div>
    </el-card>

    <el-card class="box-card">
      <el-button>默认按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
      <el-button type="success">成功按钮</el-button>
      <el-button type="info">信息按钮</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>
    </el-card>

    <!--    <img alt="Vue logo" src="./assets/logo.png">-->
    <HelloWorld msg="Welcome to Your Vue.js App - By GitHub Actions"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data () {
    return {
      circleUrl: "https://raw.githubusercontent.com/chenjunhua8080/github-page-demo/main/src/assets/logo.png",
      squareUrl: "https://raw.githubusercontent.com/chenjunhua8080/github-page-demo/main/src/assets/logo.png",
      sizeList: ["64","large", "medium", "small"],
      value: new Date(),
    }
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
  margin-top: 60px;
}
</style>


<style>
.el-card{
  margin-bottom: 30px;
}
.el-row {
  margin-bottom: 20px;
  &:last-child {
     margin-bottom: 0;
   }
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>