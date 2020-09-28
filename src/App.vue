<template>
  <div id="app">
    <get-joke/>
    <normal-joke v-if="displayType == 'normal'" key="normal"/>
    <snake-joke v-if="displayType == 'snake'"  key="snake"/>
    <loud-joke v-if="displayType == 'loud'"  key="loud"/>
  </div>
</template>

<script>
import GetJoke from "./components/getJoke.vue";
import NormalJoke from "./components/normalJoke.vue";
import SnakeJoke from "./components/snakeJoke.vue";
import LoudJoke from "./components/loudJoke";

export default {
  name: "App",
  components: {
    GetJoke,
    NormalJoke,
    SnakeJoke,
    LoudJoke
  },
  computed: {
    displayType: function(){
      return this.$store.state.displayType;
  }
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
