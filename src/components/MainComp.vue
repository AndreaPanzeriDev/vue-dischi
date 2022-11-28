<template>
  <main>
    <div class="d-flex p-5 flex-wrap">
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
      dataGenre: [],
    }
  },
  mounted() {
    this.getInfo();
  },
  methods:{

    //get data from API
    getInfo(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music').then( (response) => {
        this.dataSpotify = response.data.response;
        this.getGenre();
      } )
    },

    //create the array with all the genre
    getGenre(){
      this.dataSpotify.forEach((element)  =>{
        if(!this.dataGenre.includes(element.genre)){
          this.dataGenre.push(element.genre)
        }
      })
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