<template>
  <login msg="Welcome to Your longycc"/>
</template>

<script>
import {ref,reactive} from 'vue'
import login from "./components/Login";


export default {
  name: 'App',
  components: {
    login
  },
  methods: {
    signUp () {
    container.classList.add('right-panel-active')
    },
    signIn(){
    container.classList.remove('right-panel-active')
    }
  },
  setup(){
    function signUp () {
      container.classList.add('right-panel-active')
    }
    function signIn(){
      container.classList.remove('right-panel-active')
    }
    return {
      signUp,
      signIn
    }
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
</style>
