<script >
// import HelloWorld from './components/HelloWorld.vue'
import Conteudo from '@/components/layouts/Conteudo.vue'
import Topo from '@/components/layouts/Topo.vue'

export default {
  data: () => ({
    visibilidade: true,
  }),
  methods: {
    desmontarComponente() {
      this.visibilidade = false
    }
  },
  components: {
    Conteudo,
    Topo
  }
}


</script>

<template>
  <header>

    <div>
      <!-- <HelloWorld msg="You did it!" teste="cristian" /> -->

      <button @click="desmontarComponente()">Desmontar o componente e conteúdo</button>

      <Topo />

      <Conteudo v-if="visibilidade" />

    </div>

    <div>
      <teste ola="estou felixxx" />
    </div>
  </header>
</template>

<style scoped></style>
