<template>
  <div id="app">
    <homework65></homework65>
    <hr>
    <example81></example81>
    <hr>
    <example82></example82>
    <hr>
    <example83></example83>
  </div>
</template>

<script>
import Homework65 from './components/Homework6-5';
import Example81 from './components/Example8-1';
import Example82 from './components/Example8-2';
import Example83 from './components/Example8-3';

export default {
  name: 'app',
  components: {
    Homework65,
    Example81,
    Example82,
    Example83,
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
