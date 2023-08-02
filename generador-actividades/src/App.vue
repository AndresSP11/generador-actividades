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
  <div v-if="actividades.length>0" class="padre">
    
    <Actividades> </Actividades>
  </div>
  <p v-else class="anuncio text-center font-bold">Has realizado todas tus actividades, eres muy responsable</p>
</template>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Lobster&display=swap');
    .anuncio{
        color: rgb(245, 24, 234);
        text-shadow: 2px 2px 1px rgb(44, 36, 36);
        font-family: 'Lobster', cursive;
        font-size: 30px;
    }
    .padre{
        display: grid;
        grid-template-columns: repeat(auto-fit,minmax(300px,390px));
        gap: 10px;
        margin-top:40px;
        margin-left: 10px;
        margin-right: 10px;
        margin-bottom: 10px;
        align-items: center;
        justify-content: center;
        align-items: center;
    }
</style>

