<template>
  <div id="app">
    <HeaderComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComp
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body{
  background-color: #1e2d3b;
}
</style>
