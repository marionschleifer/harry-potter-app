<template>
  <div :key="movie.id">
    <h3>{{ movie.title }}</h3>
    <p>{{ movie.director }}</p>
    <p>{{ movie.composer }}</p>
    <span>{{ movie.release_date }}</span>
  </div>
</template>

<script>
export default {
  name: "MovieItem",
  props: ["movie"]
};
</script>
