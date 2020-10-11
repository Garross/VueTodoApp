<template>
  <div>
    <!-- first construct event then emit it up -->
    <form @submit = "AddTodo">
      <input type="text" name="inputTodo" v-model ="inputTodo" placeholder="Add Todo...">
      <input type="submit" value="submit" class = "btn">
    </form>
  </div>
</template>

<script>
//import { v4 as uuidv4 } from 'uuid';
export default {
  name: "Add Todo",
  data() {
    return{
      inputTodo: ''
    }
  },
  methods: {
    AddTodo(e) {
      e.preventDefault();
      const newTodo = {

        title: this.inputTodo,
        completed: false
      }
      //send to parent.
      this.$emit('add-todo', newTodo);

      this.inputTodo = '';
    }
  }
}
</script>

<style scoped>
form {
  display: flex;
}
input[type="text"] {
  flex: 10;
  padding: 5px;
}
input[type="submit"] {
  flex: 2;
}
</style>