<template>
  <post-form></post-form>
  <post-form></post-form>
</template>

<script>
import PostList from "./components/PostList.vue";
import PostForm from "./components/PostForm.vue";

export default {
  name: "App",
  components: {
    PostList,
    PostForm
  },
  data() {
    return {
      posts: [
        { id: 1, name: "hello", description: "Hello my name" },
        { id: 2, name: "hello1", description: "Hello my name is Yusuf"},
        { id: 3, name: "hello2", description: "Hello my name43"},
      ]
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
