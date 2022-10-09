<template>
  <PostForm @create="createPost"></PostForm>
  <PostList :posts="posts"></PostList>
</template>

<script>
import PostList from "./components/PostList.vue";
import PostForm from "./components/PostForm.vue";

export default {
  name: "App",
  components: {
    PostList,
    PostForm,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "hello", desc: "Hello my name" },
        { id: 2, title: "hello1", desc: "Hello my name is Yusuf" },
        { id: 3, title: "hello2", desc: "Hello my name43" },
      ],
    };
  },
  methods: {
    createPost(post) {
      console.log(post)
      this.posts.push(post);
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
