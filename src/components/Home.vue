<template>
  <div class="hello">
    <h1>Hello World</h1>
  </div>
</template>

<script>
// when you pass props, you want to define it here with its type
export default {
  name: "Home",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  display: flex;
}
h2 {
  color: green;
}
</style>
