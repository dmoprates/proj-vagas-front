<template>
  <div>
     <TopoPadrao />

     <h1>Componente App</h1>

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

<style scoped>

</style>
