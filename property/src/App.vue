<template>

  <div class="menu">
    <a v-for="menu in menus" :key="menu" href="#none">{{menu}}</a>
  </div>

  <div>
    <img src="">
    <h4>{{products[0]}}</h4>
    <p>100만원</p>
    <button @click="report[0]++">허위매물신고</button> <span>신고수 : {{report[0]}}</span>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>70만원</p>
    <button @click="report[1]++">허위매물신고</button> <span>신고수 : {{report[1]}}</span>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>80만원</p>
    <button @click="report[2]++">허위매물신고</button> <span>신고수 : {{report[2]}}</span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
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
</style>
