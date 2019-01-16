<template>
  <div id="app">
    <Site msg="Witaj!" today="16/01/2019" weather="sunny"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Site from "./components/Site.vue";

export default {
  name: "app",
  components: {
    Site
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
