<template>
  <div class="blog">
    <div v-if="loading">
      <Loader />
    </div>
    <div v-else>
      <h1>Blog</h1>
      <div v-for="post of posts" :key="post.id">
        <p>
          <strong>{{ post.title.rendered }}</strong>
        </p>
        <section v-html="post.content.rendered"></section>
      </div>

      <div v-if="errors && errors.length">
        <p v-for="error of errors" :key="error.id">
          {{ error.message }}
        </p>
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
      .get(`http://blog.tomfrink.com/wp-json/wp/v2/posts`)
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
