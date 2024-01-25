<script >
import PesquisarVaga from '../Comuns/PesquisarVaga.vue'
import Indicador from '../Comuns/Indicardor.vue'

export default {
    components: {
        PesquisarVaga,
        Indicador
    },
    //Ativação e desativação de componenete
    created() {
        console.log("Criado")
    },
    activated() {
        console.log('Componente Ativado')
    },
    deactivated() {
        console.log("Componente desativado")
    }
}

</script>

<template>
    <div class="container py-4">
        <div class="row">
            <PesquisarVaga />
        </div>

        <div class="row mt-5">
            <div class="col-4">
                <Indicador />
            </div>

            <div class="col-4">
                <Indicador />
            </div>

            <div class="col-4">
                <Indicador />
            </div>
        </div>
    </div>
</template>

<style scoped></style>
