<template>
  <div id="app">
   <ul>
     <li v-for="(val,index) in arr" :key="index">{{val}}</li>
   </ul>
   <button @click="revBtn">数组翻转</button>
    <button @click="sliceBtn">截取前三个</button>
     <button @click="updateBtn">更新第一个元素值</button>
  </div>
</template>

<script>


export default {
  data () {
    return {
      arr :[5,6,7,5,7,1]
    }
  },
  methods: {
    revBtn(){
      this.arr.reverse()
    },
    sliceBtn(){
      let newArr = this.arr.slice(0,3)
      this.arr = newArr
    },
    updateBtn () {
      this.$set(this.arr,0,1000)
    }
  }
  
}
</script>

<style>

</style>
