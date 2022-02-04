<template>
    <li class="list-group-item d-flex">
        <span>{{ paciente.titulo }}</span>
        <span class="espacar"></span>
        <button class="btn btn-sm mr-4" :class="classeCSS" :title="tituloBotaoConcluido">
            <i class="fa fa-check"></i>
        </button>
        <button class="btn btn-primary btn-sm mr-1" title="Editar">
            <i class="fa fa-pencil-alt"></i>
        </button>
        <button class="btn btn-danger btn-sm" title="Deletar">
            <i class="fa fa-trash"></i>
        </button>
    </li>
</template>

<script>
export default {
    props: {
        paciente: {
            type: Object,
            requred: true
        }
    },
    computed: {
        classeCSS() {
            return {
                'btn-secondary': !this.paciente.concluido,
                'btn-success': this.paciente.concluido
            }
        },
        tituloBotaoConcluido() {
            return this.paciente.concluido
                ? 'Refazer Tarefa'
                : 'Concluir Tarefa'
        }
    }
}
</script>

<style scoped>

    .espacar {
        flex: 1 1 auto;
    }

</style>

