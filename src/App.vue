<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Other target="{{target}}" />
  <Home msg="Welcome to Your Vue.js App" />
</template>

<script>
import Home from "./components/Home.vue";
import Other from "./components/Other";

// const target = "target";

export default {
  name: "App",
  components: {
    Home,
    Other,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
