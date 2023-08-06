<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Vue TodoList</h1>
  <TodoList :todos="todos" @delete-todo="DeleteTodo"/>
</template>

<script>
import TodoList from './components/TodoList.vue';

export default {
  name: 'App',
  data() {
    return {
      todos: ['Hello', 'World', 'Vue']
    }
  },
  components: {
    TodoList
  },
  methods: {
    DeleteTodo(index) {
      this.todos.splice(index, 1)
    }
  }
}
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
