<template>
  <div class="home">
    <h1>Add a review</h1>
    <div>
      Reviewer: <input type="text" v-model="newReviewReviewer">
      Rating: <input type="text" v-model="newReviewRating">
      Text: <input type="text" v-model="newReviewText">
      <button v-on:click="createReview()">Create!</button>
    </div>
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
      newReviewReviewer: "",
      newReviewRating: "",
      newReviewText: "",
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
        text: this.newReviewText,
        rating: this.newReviewRating,
        reviewer: this.newReviewReviewer
      };
      this.reviews.push(newReview);
    }
  },
  computed: {}
};
</script>
