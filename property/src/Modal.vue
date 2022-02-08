<template>
  <div class="black-bg" v-if="modalOpen == true">
    <div class="white-bg">
      <img :src="onerooms[click].image" alt="">
      <h4>{{onerooms[click].title}}</h4>
      <p>{{onerooms[click].content}}</p>
      <p>{{onerooms[click].price}}</p>
      <!-- <button @click="modalOpen = false">닫기</button> -->
    </div>
  </div>
</template>

<script>
export default {
    name: 'Modal',
    props:{
        onerooms : Array,
        click : Number,
        modalOpen : Boolean,
    }
}
</script>

<style>

</style>