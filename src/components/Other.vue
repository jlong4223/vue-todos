<template>
  <div>
    <header>This is my header</header>
    <p>{{ pcontent }}</p>
    <p>{{ user.name }}</p>
  </div>
</template>

<script>
export default {
  name: "Other",
  data() {
    return {
      pcontent: "this is the p tag",
      user: { name: "Jared" },
    };
  },
};
</script>

<style scoped></style>
