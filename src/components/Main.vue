<template>
  <main>
    <!-- <ul>
      <li v-for="(movie, index) in Movies" :key="index">
        {{ movie.title }}
      </li>
    </ul> -->

    <Movie v-for="(movie, index) in Movies" :key="index" :info="movie" />
  </main>
</template>

<script>
import axios from 'axios';
import Movie from "./Movie.vue";
export default {
  name: 'Main',
  components: {
    Movie
  },
  data() {
    return {
      APIUrl: 'https://api.themoviedb.org/3/search/movie?api_key=4b82c92c1924d290b7b7e9d2d0132a2d&query=rick',
      movies: [],
    }
  },
  created() {
    this.getMovies()
  },
  methods: {
    getMovies() {
      axios
        .get(this.APIUrl)
        .then( result => {
          // console.log(result);
          this.movies = result.data.results
        })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
