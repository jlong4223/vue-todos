<template>
  <div v-for="location in locations" v-bind:key="location.id">
    <h1>{{ location.city }}</h1>
  </div>
</template>

<script>
export default {
  name: "Locations",
  props: ["locations"],
};
</script>

<style scoped>
h1 {
  color: green;
}
</style>
