<template>
  <header class = "header">
    <h1>Todo List</h1>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </header>
</template>

<script>
  export default {
    name: "Header"
  }
</script>

<style scoped>
.header {
  background: #555;
  color: #fff;
  text-align: center;
  padding: 10px;
  border-radius: 25px;
}
.header a {
  color: #fff;
  padding-right: 5px;
  text-decoration: none;
}
</style>