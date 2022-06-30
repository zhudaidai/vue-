<template>
  <div id="app">
   <p>学生姓名</p>
   <ul>
      <li v-for="(item, index) in arr" :key="item">
          {{ index }} - {{ item }}
        </li>
   </ul>
   <ul>
     <li v-for="obj in stuArr" :key="obj.id">
       <span>{{obj.name}}</span>
       <span>{{obj.sex}}</span>
       <span>{{obj.hobby}}</span>
     </li>
   </ul>
   <p>老师信息</p>
   <div v-for="(value,key) in tObj" :key="value">{{ key }} -- {{ value }}</div>

    <p>序号</p>
      <div v-for="i in count" :key="i">{{ i }}</div>
    
  </div>
</template>

<script>


export default {
  data () {
    return {
      arr:['小王八','小乌龟','蛤蟆怪'],
      stuArr:[
        {
          id:1001,
          name:'嘤嘤怪',
          srx:'母',
          hobby:'哭哭啼啼'
        },
        {
          id:1002,
          name:'臭蛤蟆',
          srx:'公',
          hobby:'吃蚊子'
        },
        
      ],
      tObj:{
          name:'猪头',
          age:16,
          class:'hh'
        },
        count:10,
    }
  }
  
}
</script>

<style>

</style>
