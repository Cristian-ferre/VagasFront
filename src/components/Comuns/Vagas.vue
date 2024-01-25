<template>
    <div class="card">
        <div class="card-header bg-dark text-white">{{ titulo }}</div>
        <div class="card-body">
            <p>{{ descricao }}</p>
        </div>
        <div class="card-footer">
            <small class="text-muted">Salário: {{ salario }} | Modalidade: {{ modalidade }} | Tipo: {{ tipo }} | Publicação:
                {{ publicacao }}</small>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        titulo: {
            type: String,
            required: true,
            validator(t){
                if(t.length > 6) return 'Maior que 6 caracteres'
                return 'Menor que 6 caracteres'
            }
        },
        descricao: {
            type: String,
            
        },
        salario: {
            type: Number,
            required: true,
        },
        modalidade: {
            type: String,
            required: true,
        },
        tipo: {
            type: [String, Number],
            required: true,
        },
        publicacao: {
            type: String,
            required: true,
        }
    }

   
}
</script>
<style></style>