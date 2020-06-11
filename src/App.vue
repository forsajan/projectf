<template>
  <div id="app">
    <Contents msg="Welcome! Let's Learn something today!"/>
  </div>
</template>

<script>
import Contents from './components/Contents.vue'

export default {
  name: 'App',
  components: {
    Contents
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
