<template>
  <div class="blog-item">
    <a href>{{blog.title}}</a>
  </div>
</template>

<script>
export default {
  name: "BlogItem",
  props: ["blog"]
};
</script>

<style scoped>
.blog-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}
</style>

