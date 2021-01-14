<template>
  <div id="app">
    <!-- use the components here -->
    <!-- v-bind is how you pass data as props -->
    <Todos v-bind:todos="todos" />
  </div>
</template>

<script>
// import components here
import Todos from "./components/Todos";

export default {
  name: "App",
  // define components here
  components: {
    Todos,
  },
  // data is essentially the state data
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo one",
          completed: false,
        },
        {
          id: 2,
          title: "Todo two",
          completed: true,
        },
        {
          id: 3,
          title: "Todo three",
          completed: false,
        },
      ],
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
