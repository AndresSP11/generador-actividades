<script setup>
import Header from './components/Header.vue'
import Formulario from './components/Formulario.vue'
import {ref, reactive} from 'vue'
import Actividades from './components/Actividades.vue'
const actividades=ref([])

</script>

<template>
  <Header></Header>
  <Formulario></Formulario>
  <Actividades> </Actividades>
</template>
<style>

</style>

