<template>
  <div id="app">
    <HeaderComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue';
//import axios from 'axios';


export default {
  name: 'App',
  components: {
    HeaderComp
  },
  data(){
    return{
      //all the data
    }
  },
  mounted(){
    console.log("ok i'm working on it")
  },
  methods(){

  }
}
</script>



<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

body{
  background-color: #1e2d3b;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
