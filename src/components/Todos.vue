<template>
  <div class="col-8 no-gutters m-0 p-0">
    <div v-for="todo in todos" :key="todo.id">
        <TodoItem v-bind:todo="todo" />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem.vue";
export default {
  name: "Todos",
  components: {
    TodoItem,
  },
  props: ["todos"],
};
</script>

<style scoped>
</style>