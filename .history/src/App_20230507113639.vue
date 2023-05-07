<template>
  <div id="App">
     <HeaderItem />
     <TodosBox />
  </div>
</template>

<script>

import HeaderItem from "./components/Header.vue";
import TodosBox from "./components/Todos.vue";

export default {
  name: 'App',
  components: { HeaderItem, TodosBox }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
