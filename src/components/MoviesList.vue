<template>
  <div>
    <movie-item v-for="movie in movies" :key="movie.id" :movie="movie"></movie-item>
  </div>
</template>

<script>
import MovieItem from "./MovieItem";
import gql from "graphql-tag";

const GET_MOVIES = gql`
  query getMovies {
    movies {
      id
      title
      director
      composer
      release_date
    }
  }
`;

export default {
  name: "MoviesList",
  components: { MovieItem },
  data() {
    return {
      movies: []
    };
  },
  apollo: {
    movies: {
      query: GET_MOVIES
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
