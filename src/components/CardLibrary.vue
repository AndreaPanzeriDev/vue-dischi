<template>
  <div class="cards">
    <CardComp
      v-for="(elem, index) in dataSpotify"
      :key="index"
      :singleItem="elem"
      :userChoise="userChoise"
    />
  </div>
</template>

<script>
import CardComp from "./CardComp.vue";
import axios from "axios";

export default {
  components: {
    CardComp,
  },
  props: {
    userChoise: String
  },
  data() {
    return {
      //all the data
      dataSpotify: [],
      dataGenre: [],
    };
  },
  mounted() {
    this.getInfo();
  },
  methods: {
    //get data from API
    getInfo() {
      axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((response) => {
          this.dataSpotify = response.data.response;
          this.getGenre();
        });
    },

    //create the array with all the genre
    getGenre() {
      this.dataSpotify.forEach((element) => {
        if (!this.dataGenre.includes(element.genre)) {
          this.dataGenre.push(element.genre);
        }
        this.$emit('emitGenre', this.dataGenre)
      });
    },
  },
};
</script>

<style scoped lang="scss">
.cards {
  display: flex;
  flex-wrap: wrap;
}
</style>