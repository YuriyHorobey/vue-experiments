<template>
  <div id="app">
    <unlimited-grid></unlimited-grid>
    <!-- <HelloWorld/>-->
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld'
  import UnlimitedGrid from './components/unlimited-grid'

  export default {
    name: 'App',
    components: {
      UnlimitedGrid
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

  .cell {
    width: 6em;
    height: 3em;
    float: left;
    border: 1px solid #ccc;
  }

  /*Global styles*/
  div {
    box-sizing: border-box
  }
</style>
