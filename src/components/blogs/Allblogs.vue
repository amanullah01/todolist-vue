<template>
  <div>
    <div v-bind:key="blog.id" v-for="blog in blogs">
      <BlogItem v-bind:blog="blog"/>
    </div>
  </div>
</template>

<script>
import BlogItem from "./BlogItem";
export default {
  name: "Allblogs",
  props: ["blogs"],
  components: {
    BlogItem
  }
};
</script>
<style scoped>
</style>
