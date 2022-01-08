<template>
  <div v-for="post of posts" v-bind="post" v-bind:key="post.id">
    <h1>{{ post.title }}</h1>
    <h3>{{ post.body }}</h3>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "GetDataFromAPI",
  data: () => {
    return {
      url: "https://jsonplaceholder.typicode.com/posts",
      posts: [],
    };
  },

  created() {
    this.getDataAsync();
  },
  methods: {
    async getDataAsync() {
      try {
        const { data } = await axios.get(this.url);
        this.posts = data;
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>
