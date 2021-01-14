<template>
  <!-- this bind is added a class based on whether or not todo completed is true -->
  <div class="todo-item" v-bind:class="{ 'is-complete': todo.completed }">
    <p>
      <!-- v-on is how to add events -->
      <input
        type="checkbox"
        value="todo"
        @input="$emit('todo', $event.target.value)"
        v-on:change="markComplete"
      />
      {{ todo.title }}
    </p>
  </div>
</template>

<script>
// before being able to access props being passed to this component, we need to define them below
export default {
  name: "TodoItem",
  props: ["todo"],
  //   this is where you define onchange actions
  //   methods: {
  //     markComplete() {
  //       this.todo.completed = true;
  //     },
  //   },
};
</script>

<style scoped>
.todo-item {
  color: black;
  background: whitesmoke;
  border-bottom: 1px solid #ccc;
  padding: 10px;
}

.is-complete {
  text-decoration: line-through;
}
</style>
