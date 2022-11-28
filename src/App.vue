<template>
  <div id="app">
    <HeaderComp />
    <MainComp/>
  </div>
</template>

<script>
 import HeaderComp from './components/HeaderComp.vue';
 import MainComp from './components/MainComp.vue'
 


 export default { 
  name: 'App',
  components: {
    HeaderComp,
    MainComp
  },
  
 }
</script>



<style scoped lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background: #1e2d3b;
  height: 100vh;
  
}

body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
