<template>
  <div class="blog">
    <div v-if="loading">
      <Loader />
    </div>
    <div v-else>
      <h1>Blog</h1>
      <h3>
        Currently pulled from
        <a href="https://jsonplaceholder.typicode.com/"
          >jsonplaceholder.typicode.com/posts</a
        >
        REST API
      </h3>
      <div v-for="post of posts" :key="post.id">
        <hr />
        <p>
          <strong>{{ post.title }}</strong>
        </p>
        <section>{{ post.body }}</section>
        <hr />
      </div>

      <div v-if="errors && errors.length">
        <p v-for="error of errors" :key="error.id">{{ error.message }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Loader from "../components/Loader";

export default {
  components: {
    Loader
  },
  data() {
    return {
      posts: [],
      errors: [],
      loading: true
    };
  },

  // Fetches posts when the component is created.
  mounted() {
    axios
      .get(`https://jsonplaceholder.typicode.com/posts`)
      .then(response => {
        // JSON responses are automatically parsed.
        this.posts = response.data;
      })
      .catch(e => {
        this.errors.push(e);
      })
      .finally(() => {
        this.loading = false;
      });
    // async / await version (created() becomes async created())
    //
    // try {
    //   const response = await axios.get(`http://jsonplaceholder.typicode.com/posts`)
    //   this.posts = response.data
    // } catch (e) {
    //   this.errors.push(e)
    // }
  }
};
</script>
