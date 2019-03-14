<template>
  <form @submit="submit">
    <fieldset>
      <input type="text" placeholder="Title" v-model="title">
      <input type="text" placeholder="Director" v-model="director">
      <input type="text" placeholder="Composer" v-model="composer">
    </fieldset>
    <input class="button-primary" type="submit" value="Send">
  </form>
</template>

<script>
export default {
  name: "AddMovie",
  data() {
    return {
      title: "",
      director: "",
      composer: ""
    };
  },
  methods: {
    submit(e) {
      e.preventDefault();
      alert(this.$data.title);
    }
  }
};
</script>
