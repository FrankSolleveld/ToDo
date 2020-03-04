<template>
  <div id="app">
    <TextInputField v-on:addTodo="addTodo" />
    <ToDoList :todos="todos"/>

  </div>
</template>

<script>
import TextInputField from "./components/TextInputField";
import ToDoList from "./components/ToDoList";
import axios from "axios";

export default {
  name: 'App',
  components: {ToDoList, TextInputField},
  data() {
    return {
      todos: null,
    }
  },
  methods: {
    addTodo(i){
      let todo = {
        name: i,
      }
      this.todos.push(todo)
    }
  },
  created() {
    axios.get("https://jsonplaceholder.typicode.com/users")
    .then(response => {
      this.todos = response.data

      console.log(this.todos)
    })
    .catch()
  }
}
</script>

<style lang="scss">

</style>
