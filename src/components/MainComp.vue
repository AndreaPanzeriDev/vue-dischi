<template>
  <main>
    <div>
      <select class="form-select" aria-label="Default select example" v-model="optionSelected">
        <option selected>Open this select menu</option>
        <option :value="elem" v-for="(elem, index) in arrayGenre" :key="index">{{elem}}</option>
      </select>
      <CardLibrary @emitGenre="methodsGenreList" :userChoise="optionSelected"/>
    </div>
  </main>
</template>

<script>
import CardLibrary from "./CardLibrary.vue";

export default {
  name: "MainComp",
  components: {
    CardLibrary,
  },
  data(){
    return{
      arrayGenre: [],
      optionSelected : '',
    }
  },
  methods: {
    methodsGenreList(valoreEmit){
      this.arrayGenre = valoreEmit
    }
  }
};
</script>

<style scoped lang="scss">
main {
  width: 75%;
  margin: auto;
  height: 100%;
}
</style>