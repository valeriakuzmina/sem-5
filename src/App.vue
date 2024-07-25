<template>
  <div id="app">
  <productDetails />
  </div>
</template>

<script>
import productDetails from './components/productDetails.vue';

export default {
  name: 'App',
  components: {
   productDetails
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
