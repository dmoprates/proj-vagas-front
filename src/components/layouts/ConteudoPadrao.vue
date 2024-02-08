<template>
    <div>
      <h1>Componente Conteúdo</h1>

      <HomeView></HomeView>
      <PublicarVaga></PublicarVaga>
    </div>
  </template>
  
  <script>
    import HomeView from '../views/Home.vue'
    import PublicarVaga from '../views/PublicarVaga.vue'
    export default{
      name:'ConteudoPadrao',
      components: {
        HomeView,
        PublicarVaga
      }
    }
  </script>
  
  
  <style scoped>

  </style>