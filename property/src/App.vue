<template>
  <Modal :onerooms="onerooms" :click="click" :modalOpen="modalOpen"/>

  <div class="menu">
    <a v-for="menu in menus" :key="menu" href="#none">{{menu}}</a>
  </div>

  <Discount/>


 
</template>

<script>

import data from './assets/oneroom.js'
import Discount from './Discount.vue'
import Modal from './Modal.vue'

export default {
  name: 'App',
  data(){
    return {
      click : 0,
      onerooms : data,
      modalOpen : false,
      report : [0,0,0],
      menus : ['Home', 'Products', 'About'],
      products : ['역삼동원룸','천호동원룸','마포구원룸']
    }
  },
  methods :{
    increase(){
      this.report += 1
    }
  },

  components: {
    Discount,
    Modal,
  }
}
</script>

<style>
body{
  margin:0;
}
div{
  box-sizing: border-box;
}
.black-bg{
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.5);
  position: fixed;
  padding:20px;
}
.black-bg img{
  width:100%;
}
.white-bg{
  width: 100%;
  background-color: #fff;
  border-radius: 8px;
  padding: 20px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu{
  background:darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color:#fff;
  padding:10px;
}

.room-img{
  width:100%;
  margin-top:40px;
}
.discount{
  background-color: #eee;
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
}
</style>
