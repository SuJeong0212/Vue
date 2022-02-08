<template>
  <div class="black-bg" v-if="modalOpen == true">
    <div class="white-bg">
      <img :src="onerooms[click].image" alt="">
      <h4>{{onerooms[click].title}}</h4>
      <p>{{onerooms[click].content}}</p>
      <input v-model="month">
      
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
    props:{
        onerooms : Array,
        click : Number,
        modalOpen : Boolean,
    }
}
</script>

<style>

</style>