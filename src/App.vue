<template>
  <div id="app">
    <img alt="Vue log" src="./assets/logo.png">
    <h1>{{count}}</h1>
    <h1>{{double}}</h1>
    <button @click="increase">+1</button>
  </div>
</template>

<script lang="ts">
import {ref,computed} from 'vue'
export default {
  name: 'App',
  setup(){
    const count = ref(0)
    const double = computed(() => {
      return count.value*2
    })
    const increase = () =>{
      count.value++
    }
    return {
      count,
      increase,
      double
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
  margin-top: 60px;
}
</style>
