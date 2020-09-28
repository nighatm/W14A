<template>
  <div>
    <p>{{ normalJoke }}</p>
  </div>
</template>

<script>
export default {
  name: "normal-joke",
  computed: {
    normalJoke: function() {
      return this.$store.getters.normalJoke;
    }
  }
};
</script>

<style scoped>
</style>