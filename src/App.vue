<template>
  <div>
    <TopoPadrao />
    <ConteudoPadrao />
  </div>
</template>

<script>
import ConteudoPadrao from './components/layouts/ConteudoPadrao.vue'
import TopoPadrao from './components/layouts/TopoPadrao.vue'


export default {
  name: 'App',
  components: {
    ConteudoPadrao,
    TopoPadrao
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
