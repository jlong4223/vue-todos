<template>
  <div class="hello">
    <!-- the msg thing is how you pass props -->
    <h1>Hi jared {{ msg }}</h1>
    <div>
      <h2>this is from vue</h2>
    </div>
  </div>
</template>

<script>
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
