<template>
  <div id="app">
    <HelloWorld/>
    <Index />
  </div>
</template>

<script>
import './assets/css/reset.css';
import HelloWorld from './components/HelloWorld'
import Index from './components/Index'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Index
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
  margin-top: 60px;
}
</style>
