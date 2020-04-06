<template>
  <div id="app">
    <!-- <AddBlog /> -->
    <!-- <show-blogs /> -->
    <blog-header></blog-header>
    <router-view></router-view>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import AddBlog from "./components/AddBlog";
import ShowBlogs from "./components/ShowBlog";
import BlogHeader from "./components/BlogHeader";
export default {
  name: "app",
  components: {
    HelloWorld,
    AddBlog,
    ShowBlogs,
    BlogHeader
  }
};
</script>

<style>
</style>
