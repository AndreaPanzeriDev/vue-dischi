<template>
  <div class="card">
    <img :src="singleItem.poster" alt="p">
    <h1>{{ singleItem.title}}</h1>
    <div class="infoArtist"> {{ singleItem.author}}</div>
    <div class="infoArtist year"> {{ singleItem.year}}</div>
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
  width: calc(100% / 5 - 15px);
  height: 300px;
  padding: 10px;
  margin: 25px auto;
  text-align: center;
}

.card > h1{
  color: white;
  font-weight: bold;
  font-size: inherit;
  margin: auto;
  text-transform: uppercase;
}

.infoArtist{
  color: #868174;
}

.year{
  font-size: small;
}
</style>