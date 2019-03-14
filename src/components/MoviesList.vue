<template>
  <div>
    <movie-item v-for="movie in movies" :key="movie.id" :movie="movie"></movie-item>
  </div>
</template>

<script>
import MovieItem from "./MovieItem";
export default {
  name: "MoviesList",
  components: { MovieItem },
  data() {
    return {
      movies: [
        {
          id: "123123123",
          title: "Harry Potter and the Order of the Phoenix",
          director: "David Yates",
          composer: "Nicholas Hopper",
          timestamp: "123123123"
        }
      ]
    };
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
