<template>
  <div>
    <button @click="getPosts">Load Posts</button>
    <button @click="hidePosts">Hide Posts</button>
    <div v-for="post in posts" :key="post.id">
      <h3>{{ post.id }}. {{ post.title }}</h3>
      <p>{{ post.body }}</p>
      <hr />
    </div>
    <h3 v-if="errorMsg">{{ errorMsg }}</h3>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "PostList",
  // created is using when page load
  // method in life cycle hook
  created() {
    this.getPosts();
  },
  data() {
    return {
      posts: [],
      errorMsg: "",
    };
  },
  methods: {
    getPosts() {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((response) => {
          console.log(response);
          this.posts = response.data;
        })
        .catch((error) => {
          console.log(error);
          this.errorMsg = "Error retrieving data";
        });
    },
    hidePosts() {
      this.posts = [];
    },
  },
};
</script>

<style scoped></style>
