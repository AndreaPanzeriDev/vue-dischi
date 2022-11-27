<template>
  <div class="card">
    <img :src="singleItem.poster" alt="p">
    <h1>{{ singleItem.title}}</h1>
    <div class="infoArtist"> {{ singleItem.author}}</div>
    <div class="infoArtist"> {{ singleItem.year}}</div>
  </div>
</template>

<script>
export default {
  name: 'CardComp',
  props: {
    singleItem: Object
  },
  methods: {
    
  }
}
</script>

<style scoped lang="scss">

.card{
  background-color: #2e3a46;
  width: calc(100% / 5 - 5px);
  padding: 10px;
  margin: 0 2.5px;
  text-align: center;
}

.card > h1{
  color: white;
  font-weight: bold;
  font-size: inherit ;
  margin: 10px 0;
  text-transform: uppercase;
}

.infoArtist{
  color: lightgray;
}
</style>