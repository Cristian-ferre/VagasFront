

<script >
import Home from '@/components/views/Home.vue';
import PublicarVaga from '@/components/views/PublicarVaga.vue';

export default {
    components: {
        Home,
        PublicarVaga
    },
    methods: {
        AtualizarComponente() {
            this.count += 1;
            this.titulo += "!*" + this.count
        }
    },
    data: () => ({
        msg: 'O componente foi criado',
        titulo: "Componente Conteúdo",
        count: 0,
        conteudo: 'Home'
    }),
    //Faz alguma ação antes de criar um componente
    // beforeCreate() {
    //     console.log("Antes de criar", this.msg)
    // },
    //Executa alguma ação apos a criação do componentes
    // created() {
    //     console.log("Criado", this.msg)
    // },
    // beforeMount() {
    //     console.log("Antes de montar o templete")
    // },
    // mounted() {
    //     console.log("Montado")
    // },
    // beforeUpdate() {
    //     console.log("Antes de atualizar")
    // },
    // updated() {
    //     console.log("Atualizado")
    // },
    // beforeUnmount() {
    //     console.log("Antes de desmontar/destruir")
    // },
    // unmounted() {
    //     console.log("Desmontado/Destruido")
    // }
}
</script>

<template>
    <h1>{{ titulo }}</h1>
    <button @click="AtualizarComponente()">Atualizar</button>
    <button @click="conteudo = 'Home'">Home</button>
    <button @click="conteudo = 'PublicarVaga'">Publicar vaga</button>
    <KeepAlive>
        <component :is="conteudo" />
    </KeepAlive>
</template>





<style scoped></style>
