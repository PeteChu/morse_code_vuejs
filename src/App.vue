<template>
  <div id="app">
    <MorseCode/>
  </div>
</template>

<script>
import MorseCode from "./components/MorseCode";

export default {
  name: "App",
  components: { MorseCode }
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
