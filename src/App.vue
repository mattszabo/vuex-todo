<template>
  <div id="app" class="container">
    <CurrentTodos />
    <AddEditTodo />
    <CompletedTodos />
  </div>
</template>

<script>
  import AddEditTodo from './components/AddEditTodo.vue'
  import CurrentTodos from './components/CurrentTodos.vue'
  import CompletedTodos from './components/CompletedTodos.vue'

  export default {
    components: {
      AddEditTodo,
      CurrentTodos,
      CompletedTodos
    }
  }
</script>

<style>
  body {
    font-family: Helvetica, sans-serif;
  }
</style>
