<template>
  <div id="get-todo" class="container">
    <h3 v-if="isEditing">Edit Todo</h3>
    <h3 v-else>Add Todo</h3>
    <input  class="form-control"
            :value="newTodo"
            @change="setTodoText"
            placeholder="I need to..."
    >
    <button class="btn btn-primary" @click="addTodo">
      <span v-if="isEditing">Save change</span>
      <span v-else>Add Todo</span>
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    setTodoText(e) {
      this.$store.dispatch('setTodoText', e.target.value)
    },
    addTodo() {
      this.$store.dispatch('addTodo')
    }
  },
  computed: {
    newTodo() {
      return this.$store.getters.newTodo
    },
    isEditing() {
      return this.$store.getters.isEditing
    }
  }
}
</script>
