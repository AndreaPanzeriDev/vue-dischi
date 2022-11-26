<template>
  <div class="card">
    <img :src="singleItem.poster" alt="poster">
    <h1>{{ singleItem.year }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    singleItem: Object,
  },
  methods: {
    
  }
}
</script>

<style scoped>

.card{
  background-color: #2e3a46;
  padding: 10px;
  width: calc(100% / 6 - 5px);
  margin: 0 2.5px;
  text-align: center;
}

.card > h2{
  color: white;
  font-weight: bold;

}
</style>