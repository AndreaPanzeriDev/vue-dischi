<template>
  <main>
    <div>
      <select class="form-select" aria-label="Default select example">
        <option selected>Open this select menu</option>
        
      </select>
      <CardLibrary />
    </div>
  </main>
</template>

<script>
import CardLibrary from "./CardLibrary.vue";

export default {
  components: {
    CardLibrary,
  },
};
</script>

<style scoped lang="scss">
main {
  width: 75%;
  margin: auto;
  height: 100%;
}
</style>