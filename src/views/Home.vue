<template>
  <div class="home">
    <h1>Add a review</h1>
    <button v-on:click="createReview()">Create!</button>
    <h1>Reviews</h1>
    <div v-for="review in reviews">
      <h3>{{ review.reviewer }} - {{ review.rating }}</h3>
      <p>{{ review.text }}</p>
    </div>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      peter: "yo",
      reviews: [
        {
          id: 1,
          text: "Vue.js is the best thing since sliced bread!",
          rating: 5,
          reviewer: "Burton Wax"
        },
        {
          id: 2,
          text: "I love Vue.js, especially when I'm programming!",
          rating: 4,
          reviewer: "Emily Post"
        },
        {
          id: 3,
          text: "Vue.js is waaaaay better than Chinese Checkers.",
          rating: 2,
          reviewer: "Angela Pearson"
        }
      ]
    };
  },
  created: function() {},
  methods: {
    createReview: function() {
      var newReview = {
        id: 5,
        text: "...whoa...",
        rating: 5,
        reviewer: "Keanu Reeves"
      };
      this.reviews.push(newReview);
    }
  },
  computed: {}
};
</script>
