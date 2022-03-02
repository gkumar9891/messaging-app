<template>
  <div id="app">
    <MessangerArea />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

import MessangerArea from "./components/Messanger.vue";

export default {
  name: "App",
  components: {
    MessangerArea,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
