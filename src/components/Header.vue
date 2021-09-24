<template>
  <header>
    <h1>{{ msg }}</h1>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/generals";
@import "../style/vars";

header {
  width: 100%;
  height: 80px;
  background-color: $black;
  display: flex;
  align-items: center;

  h1 {
    padding: 20px;
    color: $red;
  }
}

</style>
