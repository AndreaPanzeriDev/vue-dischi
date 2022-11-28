<template>
  <header>
    <div>
      <img src="../assets/img/Spotify_logo_without_text.svg.png" alt="logo" />
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComp",
};
</script>

<style  scoped lang="scss">
header {
  display: flex;
  align-items: center;
  background-color: #2e3a46;
}

header > div > img {
  width: 100px;
  padding: 10px 20px;
}

</style>