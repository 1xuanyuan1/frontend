<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Child1 msg="Welcome to Your Vue.js App" />
    <Child2 foo="helo" @click="test" @mousemove="move"/>

    <MForm :rules="rules" :model="userinfo">
      <MFormItem label="用户名">
        <MInput v-model="userinfo.username"></MInput>
      </MFormItem>
    </MForm>
    
  </div>
</template>

<script>
import Child1 from './components/child1.vue'
import Child2 from './components/child2.vue'

import MForm from '@/slots/MForm.vue'
import MFormItem from '@/slots/MFormItem.vue'
import MInput from '@/slots/MInput.vue'
export default {
  name: 'App',
  components: {
    Child1,
    Child2,
    MForm,
    MFormItem,
    MInput
  },
  data() {
    return {                             
      userinfo: {
        username: '',
        password: ''
      },
      rules: {
        username: [{ required: true, message: "请输入用户名" }], 
        password: [{ required: true, message: "请输入密码" }]
      }
    }
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
