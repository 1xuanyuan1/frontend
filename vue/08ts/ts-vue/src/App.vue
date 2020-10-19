<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
    {{book.name}} - {{book.anthor}}
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

interface Book {
    name: string,
    anthor: string,
    page: number
}

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld
  },
  data () {
    return {
      book: {
        name: '斗破苍穹',
        anthor: '天蚕土豆'
      } as Book
    }
  },
})
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
