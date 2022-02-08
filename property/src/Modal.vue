<template>
  <div class="black-bg" v-if="modalOpen == true">
    <div class="white-bg">
      <img :src="onerooms[click].image" alt="">
      <h4>{{onerooms[click].title}}</h4>
      <p>{{onerooms[click].content}}</p>
      <input v-model.number="month">
      
      <p>{{month}}개월 선택함{{onerooms[click].price * month}}</p>

      <button @click="$emit('closeBtn')">닫기</button>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Modal',
    data(){
        return{
            month:1,
        }
    },
    watch :{
      month(a){
        if(a >= 13){
          alert('13이상 입력 노노')
        }
        if(isNaN(a) == true){
          alert('문자입력 노노')
          this.month = 1
        }
      }
    },
    props:{
        onerooms : Array,
        click : Number,
        modalOpen : Boolean,
    }
}
</script>

<style>

</style>