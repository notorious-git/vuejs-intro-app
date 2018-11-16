<template>
  <div class="home">
    <h1>{{ message + peter }}</h1>
    <h2>{{ 2 * 4 }}</h2>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      peter: "yo"
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>
