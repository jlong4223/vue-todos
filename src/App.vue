<template>
  <div id="app">
    <!-- use the components here -->
    <!-- v-bind is how you pass data as props -->
    <Todos v-bind:todos="todos" />
    <Locations v-bind:locations="locations" />
  </div>
</template>

<script>
// import components here
import Todos from "./components/Todos";
import Locations from "./components/Locations";

export default {
  name: "App",
  // define components here
  components: {
    Todos,
    Locations,
  },
  // data is essentially the state data
  data: () => ({
    error: "",
    locations: [],

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
  }),
  // this is how you fetch data from API using ajax
  mounted() {
    fetch("https://brewery-advisor-api.herokuapp.com/locations")
      .then((res) => res.json())
      .then((result) => {
        this.locations = result;
      });
  },
  methods: {},
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
