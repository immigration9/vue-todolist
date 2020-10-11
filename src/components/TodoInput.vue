<template>
  <div>
    <input v-model="newTodoItem" @keyup.enter="addTodo" />
    <button @click="addTodo">Add</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoItem: "",
    };
  },
  methods: {
    addTodo() {
      if (this.newTodoItem) {
        this.$emit("add-todo-to-list", this.newTodoItem);
        this.newTodoItem = "";
      }
    },
  },
};
</script>
