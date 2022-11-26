<template>
  <div id="app">
    <HeaderComp />
  </div>
</template>

<script>
 import HeaderComp from './components/HeaderComp.vue';
 import axios from 'axios';


 export default { 
  name: 'App',
  components: {
    HeaderComp
  },
  data(){
    return{
      //all the data
      dataSpotify: '',
    }
  },
  mounted() {
    this.getInfo();
  },
  methods:{
    
    getInfo(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music').then( (response) => {
        this.dataSpotify = response.data
      } )
    }
  }
 }
</script>



<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

body {
  background-color: #1e2d3b;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
