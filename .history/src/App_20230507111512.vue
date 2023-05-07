<template>
  <div id="App">
     <HeaderItem />
     <Todos />>
  </div>
</template>

<script>

import HeaderItem from "./components/Header.vue";
import Todos from "./components/Todos.vue";

export default {
  name: 'App',
  components: {
     HeaderItem, Todos
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
