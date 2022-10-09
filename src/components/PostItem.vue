<template>
  <div class="parent" v-for="post in posts">
    <div>
      <div class="text"><strong>Название</strong> {{post.title}}</div>
      <div class="text"><strong>Описание</strong> {{post.desc}}</div>
    </div>
    <div>
      <my-button @click="">Удалить</my-button>
    </div>
  </div>
</template>

<script>
import MyButton from "@/components/UI/MyButton";
export default {
  name: "PostList",
  components: {MyButton},
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