<template>

  <div class="movies_cont">
    <ul>
      <li>
        
        <div> {{ info.title }} </div>
        <div> {{ info.original_title }} </div>

        <div class="center">
          <div class="flag_cont"> 
        
            <img :src="require(`../assets/img/${info.original_language}.jpg`)" alt="info.original_language"> 
        
          </div>
        </div>

        <div> {{ info.vote_average }} </div>
        
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'Movie',
  props: ['info'],
  data: function () {
    return {
      flags: ["en", "de", "ja"]
    }
  }
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

    li .center {
      display: flex;
      justify-content: center;

      .flag_cont {
      width: 30px;
      height: 20px;

        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}

</style>
