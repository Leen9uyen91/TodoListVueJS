<template>
  <div id="App">
     <HeaderItem />
     <Todos />>
  </div>
</template>

<script>

import HeaderItem from "./components/Header.vue";
import TodosItem from "./components/Todos.vue";

export default {
  name: 'App',
  components: {
     HeaderItem, TodosItem
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
