<template>
  <div id="app">
    <MassAdducts/>
  </div>
</template>

<script>
import MassAdducts from "./components/MassAdducts";

export default {
  name: "App",
  components: {
    MassAdducts
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
  margin-top: 40px;
}
</style>
