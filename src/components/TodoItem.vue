<template>
  <div class="todo-item">
    <p>{{ todo.title }}</p>
  </div>
</template>

<script>
// before being able to access props being passed to this component, we need to define them below
export default {
  name: "TodoItem",
  props: ["todo"],
};
</script>

<style scoped>
.todo-item {
  color: black;
  background: whitesmoke;
  border-bottom: 1px solid #ccc;
  padding: 10px;
}
</style>
