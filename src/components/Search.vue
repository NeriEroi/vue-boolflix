<template>
  <form>
    <div>
      <input type="text" class="" placeholder="Search Movie" v-model='inputText'>
    </div>

    <div>
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

</style>
