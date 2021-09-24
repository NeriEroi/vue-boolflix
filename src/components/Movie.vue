<template>

  <div class="movies_cont">
    <ul>
      <li>
        
        <div> {{ info.title }} </div>
        <div> {{ info.original_title }} </div>
        <div> {{ info.original_language }} </div>
        <div> {{ info.vote_average }} </div>
        
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'Movie',
  props: ['info']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/generals";
@import "../style/vars";

.movies_cont {
  width: 19%;
  padding: 5px;
  margin:5px;
  background-color: #00000075;

  ul {
    list-style-type: none;
    text-align: center;
  }
}

</style>
