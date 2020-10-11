<template>
  <ul>
    <todo v-for="(item, index) in todos" :key="index" :todo="item" />
  </ul>
</template>

<script>
import Todo from "./Todo.vue";

export default {
  components: {
    Todo,
  },
  props: {
    todos: Array,
  },
};
</script>
