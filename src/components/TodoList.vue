<template>
  <ul>
    <li v-for="(todo, index) in todos" :key="todo.id" @click="deleteTodo(index)">{{index+1}}. {{todo}}</li>
  </ul>
</template>

<script>
export default {
  props: ['todos'],
  methods: {
    deleteTodo(index) {
      this.$emit('delete-todo', index)
    }
  }
}
</script>

<style scoped>
  ul {
    list-style: none;
    padding: 0;
    cursor: pointer;
  }
</style>