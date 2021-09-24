<template>
  <main>

    <Search @performSearch="searchMovie"/>

    <Movie v-for="(movie, index) in filteredMovies" :key="index" :info="movie" />

  </main>
</template>

<script>
import axios from 'axios';
import Movie from "./Movie.vue";
import Search from "./Search.vue"
export default {
  name: 'Main',
  components: {
    Movie,
    Search
  },
  data() {
    return {
      APIUrl: 'https://api.themoviedb.org/3/search/movie?api_key=4b82c92c1924d290b7b7e9d2d0132a2d&query=rick',
      movies: [],
      movieText: ''
    }
  },
  created() {
    this.getMovies()
  },
  computed: {
    filteredMovies() {
      if (this.movieText === '') {
        return this.movies
      }

      let filteredMovie = this.movies.filter( item => {
        return item.title.toLowerCase().includes(this.movieText.toLowerCase());
      })

      return filteredMovie;
    }
  },
  methods: {
    getMovies() {
      axios
        .get(this.APIUrl)
        .then( result => {
          // console.log(result);
          this.movies = result.data.results
        })
    },
    searchMovie(text) {
      this.movieText = text;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
