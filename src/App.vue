<template>
  <div id="app">
    <todo-input :add-todo="addTodoToList" @add-todo-to-list="addTodoToList" />
    <todo-list :todos="todos" />
  </div>
</template>

<script>
import TodoInput from "./components/TodoInput.vue";
import TodoList from "./components/TodoList.vue";

export default {
  name: "App",
  components: {
    TodoInput,
    TodoList,
  },
  data() {
    return {
      todos: ["Pickup groceries", "Go meet friends", "Start learning Vue"],
    };
  },
  methods: {
    addTodoToList(newTodoItem) {
      this.todos = this.todos.concat(newTodoItem);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
