<template>
  <div id="app">
    <transition :name="flag==true?'van-slide-up':'1'">
      <div v-show="flag" class="box">1122</div>
    </transition>
    <div class="buttons">
    <van-button type="default" @click="changeType">默认按钮</van-button>
    <van-button type="primary">主要按钮</van-button>
    <van-button type="info">信息按钮</van-button>
    <van-button type="warning">警告按钮</van-button>
    <van-button type="danger">危险按钮</van-button> 
     </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: "App",
  data(){
    return{
      flag:false
    }
  },
  methods:{
    changeType(){
      this.flag=!this.flag;
      console.log(this.flag)
      
    }
  }
};
</script>

<style  lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.box {
  width: 200px;
  height: 200px;
  background: cadetblue;
  font-size: 25px;
  position:absolute;
  margin: 200px auto auto;
}
.buttons{
  width: 100%;
}
</style>
