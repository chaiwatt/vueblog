<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld title="Cat" msg="Hello Cat" link="www.cat.com" />
    <HelloWorld title="Big Cat" msg="Hello Big Cat" link="www.bigcat.com" />
    <HelloWorld title="Bigger Cat" msg="Hello Bigger Cat" link="www.biggercat.com" />
    <HelloWorld title="The Bigest Cat" msg="Hello Biggest Cat" link="www.biggestcat.com" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
