<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Child1 msg="Welcome to Your Vue.js App" />
    <Child2 foo="helo" @click="test" @mousemove="move"/>
  </div>
</template>

<script>
import Child1 from './components/child1.vue'
import Child2 from './components/child2.vue'

export default {
  name: 'App',
  components: {
    Child1, Child2
  },
  methods: {
    test () {
      console.log('老爸呼唤儿子')
    },
    move () {
      console.log('老爸抚摸儿子')
    }
  },
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
