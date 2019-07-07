<template>
  <div>
    <h1>Blog</h1>
    <Allblogs v-bind:blogs="blogs"/>
  </div>
</template>

<script>
import Allblogs from "../components/blogs/Allblogs";
import axios from "axios";
export default {
  name: "blog",
  components: {
    Allblogs
  },
  data() {
    return {
      blogs: []
    };
  },
  created() {
    axios
      .get("https://jsonplaceholder.typicode.com/posts")
      .then(res => (this.blogs = res.data))
      .catch(err => console.log(err));
  }
};
</script>


<style scoped>
</style>

