<template>
  <form>

    <div class="input_cont">
      <input type="text" class="" placeholder="Search Movie" v-model='inputText'>
    </div>

    <div class="button_cont">

      <button type="submit" class="" @click.prevent="$emit('performSearch', inputText)">
        Search
      </button>

    </div>
    
  </form>
</template>

<script>

export default {
  name: 'Search',
  data() {
    return {
      inputText: '',
    }
  },
  methods: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/generals";
@import "../style/vars";

form {
  width: 100%;
  height: 65px;
  padding: 10px;
  background-color: $lightgrey;
  display: flex;
  justify-content: flex-end;
  align-items: center;

  .input_cont {
    margin: 10px;
    
    input {
      padding: 10px;
    }
  }

  .button_cont button {
    background-color: $red;
    border: none;
    border-radius: 10px;
    color: white;
    padding: 10px;
    font-size: 15px;
  }
}

</style>
