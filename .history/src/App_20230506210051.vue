<template>
  <div id="App">
     <p>Đây là app vue đầu tiên của tôi</p>
     <HeaderItem />
  </div>
</template>

<script>

import HeaderItem from "./components/Header.vue";

export default {
  name: 'App',
  components: {
     HeaderItem
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
  margin-top: 60px;
}
</style>
