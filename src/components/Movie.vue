<template>
  <main>
    <ul>
      <li>
        
        <div> {{ info.title }} </div>
        <div> {{ info.original_title }} </div>
        <div> {{ info.original_language }} </div>
        <div> {{ info.vote_average }} </div>
        
      </li>
    </ul>
  </main>
</template>

<script>

export default {
  name: 'Movie',
  props: ['info']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
