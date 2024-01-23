<script >

export default {
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
            <div class="col">
                <p> Home </p>
                <div class="h-100 p-5 bg-light border rounded-3"></div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>
