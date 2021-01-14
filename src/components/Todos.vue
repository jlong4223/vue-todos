<template>
  <div>
    <!-- using v-for as a way to loop through the todos array which is defined in props
      defining todo as the parameter which could be named anything
      need v-bind:key for this
      I am passing props again to the next component
       -->
    <div v-for="todo in todos" v-bind:key="todo.id">
      <TodoItem v-bind:todo="todo" />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem.vue";

// name is the component name that you want to export
export default {
  name: "Todos",
  components: {
    TodoItem,
  },
  props: ["todos"],
};
</script>

<style lang="stylus" scoped></style>
