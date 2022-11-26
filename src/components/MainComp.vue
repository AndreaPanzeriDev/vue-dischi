<template>
  <main>
    <div class="d-flex p-5">
        <CardComp v-for="(element, index) in dataSpotify" :key="index" :singleItem="element"
        />
    </div>
  </main>
</template>

<script>

import CardComp from './CardComp.vue';
import axios from 'axios';

export default {
  components:{
    CardComp
  },
  data(){
    return{
      //all the data
      dataSpotify: [],
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

<style scoped lang="scss">

main{
    width: 75%;
    margin: auto;
}

</style>