<template>
  <div>
    <!-- using v-for as a way to loop through the todos array which is defined in props
      defining todo as the parameter which could be named anything
      need v-bind:key for this
       -->
    <div v-for="todo in todos" v-bind:key="todo.id">
      <h3>{{ todo.title }}</h3>
    </div>
  </div>
</template>

<script>
// name is the component name that you want to export
export default {
  name: "Todos",
  props: ["todos"],
};
</script>

<style lang="stylus" scoped></style>
