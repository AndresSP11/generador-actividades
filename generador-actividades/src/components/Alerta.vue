<script setup>
    
    const props = defineProps({
        alerta:{
            type:Object,
            required:true
        }
    })
</script>
<template>
    <div class=" bg-red-600 w-full rounded-lg shadow-lg text-center uppercase font-bold py-2 mb-4">

        {{ alerta.mensaje }}
    </div>
    
</template>
<style>
</style>