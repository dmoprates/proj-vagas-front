<template>
  <div>
    <vagas-favoritas></vagas-favoritas>
    <topo-padrao @navegar="componente = $event"/>
    <alerta-view v-if="exibirAlerta">
      <template v-slot:titulo>
        <h5>Título do alerta</h5>
      </template>
      <template v-slot:descricao>
        <p>Descrição do alerta</p>
      </template>
    </alerta-view>
    <conteudo-padrao v-if="visibilidade" :conteudo="componente"></conteudo-padrao>
  </div>
</template>

<script>
import AlertaView from './components/comuns/Alerta.vue'
import ConteudoPadrao from './components/layouts/ConteudoPadrao.vue'
import VagasFavoritas from './components/comuns/VagasFavoritas.vue'
import TopoPadrao from './components/layouts/TopoPadrao.vue'


export default {
  name: 'App',
  data: () => ({
    visibilidade: true,
    componente: 'Home',
    exibirAlerta: false
  }),
  methods: {
    desmontarComponente() {
      this.visibilidade = false
    },
    acao(p){
      console.log(p)
    }
  },
  components: {
    AlertaView,
    ConteudoPadrao,
    TopoPadrao,
    VagasFavoritas
  },
  mounted() {
    this.emitter.on('alerta', () => {
      this.exibirAlerta = true
      setTimeout(() => this.exibirAlerta = false, 4000)
      console.log('mensagem customizada')
    })
  }
}
</script>

<style scoped>

</style>
