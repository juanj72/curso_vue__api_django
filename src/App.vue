<template>
  <img alt="Vue logo" src="./assets/logo.png">

  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <hr>

  <MenuInicio msg="hola desde mi componente"/>
  <hr>
  


</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MenuInicio from './components/MenuInicio.vue';


export default {
  name: 'App',
  components: {
    HelloWorld,
    MenuInicio
    
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
hr{
  border-top: 1px solid rgb(187, 15, 15);
}
</style>
