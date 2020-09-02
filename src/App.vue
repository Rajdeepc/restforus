<template>
  <div id="app">
    <HeroBanner msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HeroBanner from './components/HeroBanner.vue'

export default {
  name: 'app',
  components: {
    HeroBanner
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
