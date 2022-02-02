<template>
    <div>

        <h1 class="font-weight-light">Lista de Pacientes</h1>

        <ul class="list-group" v-if="pacientes.length > 0">
            <PacientesListaIten
                v-for="paciente in pacientes"
                :key="paciente.id"
                :paciente="paciente" />
        </ul>

        <p v-else>Sem pacientes na lista.</p>


    </div>
</template>

<script>
import axios from 'axios'

import config from './config/config'
import PacientesListaIten from './PacientesListaIten.vue'

export default {
    components: {
        PacientesListaIten
    },
    data() {
        return {
            pacientes: [
            ]
        }
    },
    created(){
        axios.get('${config.apiURL}/pacientes')
        .then((response) => {
            console.log
        })
    }
}
</script>
