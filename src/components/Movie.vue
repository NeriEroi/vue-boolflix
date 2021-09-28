<template>

  <div class="movies_cont">
    <ul>
      <li>

        <div class="center_poster">

          <div class="poster_cont">
            <img :src="`https://image.tmdb.org/t/p/w342${info.poster_path}`" :alt="info.poster_path">
          </div>

        </div>
        
        <div><span style="color:blue;">TITLE:</span> {{ info.title }} </div>
        <div><span style="color:blue;"> ORIGINAL TITLE:</span> {{ info.original_title }} </div>

        <div class="center_flag">
          <div class="flag_cont">
        
            <img :src="require(`../assets/img/${info.original_language}.jpg`)" :alt="info.original_language">
        
          </div>
        </div>

        <div><span style="color:blue;">VOTE: </span> {{ info.vote_average }} </div>
        
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
  height: 500px;
  padding: 10px 5px;
  margin:5px;
  background-color: yellow;

  ul {
    list-style-type: none;
    text-align: center;

    li .center_poster {
      display: flex;
      justify-content: center;

      .poster_cont {
        width: 250px;
        height: 350px;
        margin-bottom: 5px;

        img {
          width: 100%;
          height: 100%;
        }
      }
    } 

    li .center_flag {
      display: flex;
      justify-content: center;

      .flag_cont {
        width: 30px;
        height: 20px;
        margin: 5px;

        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}

</style>
