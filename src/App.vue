<template>
  <div id="app">
    <ItemInput />
    <ToDoList :todos="todos"/>

  </div>
</template>

<script>
import ItemInput from "./components/ItemInput";
import ToDoList from "./components/ToDoList";
import axios from "axios";

export default {
  name: 'App',
  components: {ToDoList, ItemInput},
  data() {
    return {
      todos: null,
    }
  },
  created() {
    axios.get("https://jsonplaceholder.typicode.com/todos")
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
