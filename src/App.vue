<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="This is Vue Study"/>
  <TodoApp />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TodoApp from './components/Todo.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TodoApp
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
