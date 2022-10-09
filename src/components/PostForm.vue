<template>
  <div>
    <h3>Создание поста</h3>
    <myinput v-model="post.title" placeholder="Название"></myinput>
    <myinput v-model="post.desc" placeholder="Описание"></myinput>
    <my-button @click="createPost">Создать</my-button>
  </div>
</template>

<script>
export default {
  name: "PostForm",
  data() {
    return{
      post: {
        title: "",
        desc: ""
      }
    }
  },
  methods: {
    createPost() {
        this.post.id = Date.Now,
        this.$emit("create", this.post),
        this.post = {
          title: '',
          desc: ''
      }
    }
  }
}
</script>

<style scoped>

</style>