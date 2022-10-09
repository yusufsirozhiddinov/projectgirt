<template>
  <button><slot></slot></button>
</template>

<script>
export default {
  name: "MyButton"
}
</script>

<style scoped>
  button{
    width: 100px;
    height: 50px;
    border: none;
    background: transparent;
    font-size: 14px;
    border: 2px solid dodgerblue;
  }
</style>