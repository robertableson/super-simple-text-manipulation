<template>
  <div id="app">
    <img alt="Vue logo" class="top-logo" src="./assets/logo.png">
    <Title message="Super simple text manipulation"/>
    <Tools/>
  </div>
</template>

<script>
  import Title from './components/Title.vue'
  import Tools from './components/Tools/Tools.vue'

  export default {
    name: 'App',
    components: {
      Title,
      Tools
    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    text-align: center;
    margin-top: 60px;
  }

  #app .top-logo{
    max-width: 100px; 
  }
</style>
