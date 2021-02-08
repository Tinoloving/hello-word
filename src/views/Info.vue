<template>
  <div>
    hello Info
    <button type="button" @click="add()">添加</button>
  </div>
</template>

<script>
import store from '@/store'
  export default {
    name: "Info",
    store,
    data (){
      return {
        msg: 'hello msg'
      }
    },
    mounted() {//vue生命周期
      window.vue = this  //此句代表的是Info组件，可在调试器中通过window.vue.**（方法名）调用
    },
    methods: {
      add(){
        console.log('add Event from Info');
        //debugger  //断点
        store.commit('increase');
      }
    }
  }
</script>

<style scoped>

</style>
