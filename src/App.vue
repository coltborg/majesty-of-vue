<template>
  <div id="app">
    <hello></hello>
    <hr>
    <homework65></homework65>
  </div>
</template>

<script>
import Hello from './components/Hello';
import Homework65 from './components/Homework6-5';

export default {
  name: 'app',
  components: {
    Hello,
    Homework65,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
