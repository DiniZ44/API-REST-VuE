<template>
  <div id="app">

    <div class="jumbotron jumbotron-fluid">
      <div class="container">
        <h1 class="display-4">Consulta Pacientes</h1>
        <p class="lead"> Utilizando a Biblioteca AXIOS fazendo requisições Ajax a uma API REST, referente ao desafio da Anlix.</p>
      </div>
    </div>

    <div class="container"> 

      <PacientesLista />

    </div>

  </div>
</template>

<script>
import  PacientesLista from './components/PacientesLista.vue'

export default ({
  components: {
    PacientesLista
  }
})
</script>