<template>
  <div>
      <post-item v-for="post in posts" :post="post" :key="post.id"></post-item>
  </div>
</template>

<script>
import MyButton from "@/components/UI/MyButton";
import PostItem from "@/components/PostItem";
export default {
  name: "PostList",
  components: {PostItem, MyButton},
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>
.parent{
  padding: 20px;
  margin: 20px;
  border: 2px solid dodgerblue;
}
  .text{
    text-align: left;
  }
</style>