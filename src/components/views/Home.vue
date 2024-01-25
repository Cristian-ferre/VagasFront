<script >
import PesquisarVaga from '../Comuns/PesquisarVaga.vue'
import Indicador from '../Comuns/Indicardor.vue'
import Vaga from '../Comuns/Vagas.vue'

export default {
    components: {
        PesquisarVaga,
        Indicador,
        Vaga
    },
    data: () => ({
        vagas: [
            {
                titulo: 'Desenvolvedor Full Stack',
                descricao: 'O profissional será responsável pelo desenvolvimento de aplicações web.',
                salario: 6000,
                modalidade: 'CLT',
                tipo: 'Tempo Integral',
                publicacao: '25-01-2024'
            },
            {
                titulo: 'Designer Gráfico',
                descricao: 'Procuramos um designer criativo para desenvolver materiais visuais impactantes.',
                salario: 4500,
                modalidade: 'Freelance',
                tipo: 'Projeto',
                publicacao: '26-01-2024'
            },
            {
                titulo: 'Analista de Marketing Digital',
                descricao: 'Buscamos um profissional para gerenciar campanhas online e redes sociais.',
                salario: 5500,
                modalidade: 'PJ',
                tipo: 'Tempo Integral',
                publicacao: '27-01-2024'
            },
            {
                titulo: 'Engenheiro de Software',
                descricao: 'O engenheiro será responsável pelo desenvolvimento e manutenção de software.',
                salario: 7000,
                modalidade: 'CLT',
                tipo: 'Tempo Integral',
                publicacao: '28-01-2024'
            },
            {
                titulo: 'Assistente Administrativo',
                descricao: 'Auxiliar nas atividades administrativas do escritório.',
                salario: 3500,
                modalidade: 'Estágio',
                tipo: 'Meio Período',
                publicacao: '29-01-2024'
            },
            {
                titulo: 'Analista de Suporte Técnico',
                descricao: 'Prestar suporte técnico aos usuários internos e externos.',
                salario: 5000,
                modalidade: 'CLT',
                tipo: 'Tempo Integral',
                publicacao: '30-01-2024'
            }
        ]
    }),
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
            <PesquisarVaga titulo="Vagas abertas" indicador="100" />
        </div>

        <div class="row mt-5" v-for="( vaga, index ) in vagas" :key="index">
            <div class="col">
                <!-- Antes  -->
                <!-- <Vaga :titulo="vaga.titulo" :descricao="vaga.descricao" :salario="vaga.salario"
                    :modalidade="vaga.modalidade" :tipo="vaga.tipo" :publicacao="vaga.modalidade" /> -->

                <!-- Depois -->
                <Vaga v-bind="vaga" />
            </div>
        </div>

        <div class="row mt-5">
            <div class="col-4">
                <Indicador titulo="Vagas abertas" indicador="100" bg="bg-ligth" color="text-dark" />
            </div>

            <div class="col-4">
                <Indicador titulo="Profissionais cadastrados" indicador="225" bg="bg-dark" color="text-white" />
            </div>

            <div class="col-4">
                <Indicador titulo="Visitantes online" indicador="25" bg="bg-ligth" color="text-dark" />
            </div>
        </div>
    </div>
</template>

<style scoped></style>
