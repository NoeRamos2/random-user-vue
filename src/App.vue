<template>
  <div id="app">
    <User></User>
  </div>
</template>

<script>
import User from "./components/User.vue";

export default {
  name: "App",
  components: {
    User,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #263238;
  color: #ffffff;
  margin-top: 60px;
}
</style>
