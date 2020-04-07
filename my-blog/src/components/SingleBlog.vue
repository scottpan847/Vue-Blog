<template>
  <div id="single-blog">
    <div>
      <img :src="imgUrl" alt="icon">
    </div>
    <h1>{{blog.title}}</h1>
    <article>{{blog.body}}</article>
  </div>
</template>

<script>
export default {
  name: "single-blog",
  data() {
    return {
      id: this.$route.params.id,
      blog: {},
      imgUrl:""
    };
  },
  created() {
    let urlTemp="assets/logo.png";
    this.imgUrl = require("@/"+urlTemp)
    this.$http
      .get("http://localhost:3000/posts/" + this.id)
      .then(function(data) {
        //console.log(data);
        this.blog = data.body;
      });
  }
};
</script>
<style scoped>
#single-blog {
  max-width: 960px;
  margin: 0 auto;
  padding: 20px;
  background: #eee;
  border: 1px dotted #aaa;
}
</style>