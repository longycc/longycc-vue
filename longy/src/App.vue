<template>
  <h1>组件</h1>
  <h2>name:{{job.type}}</h2>
  <h2>年龄age:{{job.salary}}</h2>
  <button @click="changeInf">修改人信息</button>
</template>

<script>
import {ref,reactive} from 'vue'

export default {
  name: 'App',
  setup(){
    let name = ref('longy')
    let age = ref(10)
    let job = reactive({
      type:"js",
      salary:"250"
    })
    function changeInf(){
      job.salary = 8000
    }
    return {
      name,
      age,
      changeInf,
      job,
    }
  }
}
</script>

<style>
/*#app {*/
/*  font-family: Avenir, Helvetica, Arial, sans-serif;*/
/*  -webkit-font-smoothing: antialiased;*/
/*  -moz-osx-font-smoothing: grayscale;*/
/*  text-align: center;*/
/*  color: #2c3e50;*/
/*  margin-top: 60px;*/
/*}*/
</style>
