<template>
  <div id="app">
    <product></product>
    
  </div>
</template>

<script>
import Product from "./Product.vue";


export default {
  name: 'App',
  components: {
    Product
    
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
