<script setup>
    import { computed } from 'vue'
    const props = defineProps({
        alerta:{
            type:Object,
            required:true
        }
    })
    const isError=computed(()=>{
        if(props.alerta.tipo==='error'){
            return 'bg-green-600'
        }else{
            return 'bg-red-800'
        }
    })
</script>
<template>
    <div :class="isError" class="w-full rounded-lg shadow-lg text-center uppercase font-bold py-2 mb-4 text-white" >
        {{ alerta.mensaje }}
    </div>
    
</template>
<style>
</style>