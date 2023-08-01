<script setup>
    import { reactive } from 'vue'
    const alerta= reactive({
        mensaje:'',
        tipo:''
    }) 

    const tarea=reactive({
        nombre:"",
        fecha:"",
        asunto:""
    })

    const validar=()=>{
        if(Object.values(tarea).includes("")){
            
        }
        console.log("Validando")
    }
</script>
<template>
    <div class="contenedor-formulario">
        <form class="formulario shadow-md shadow-green-200 rounded-md w-96">
            <div>
                <label class="labeldiv font-bold text-green-900 uppercase ">
                    Actividad a realizar
                </label>
                <input type="text" 
                placeholder="Coloque aqui su actividad"
                class="label-input w-full my-2 rounded-md px-2 py-1"
                v-model="tarea.nombre"
                >
            </div>
            <div>
                <label class="labeldiv font-bold text-green-900 uppercase">
                    Fecha a realizar
                </label>
                <input type="date" 
                class="label-input w-full my-2 rounded-md px-2 py-1"
                v-model="tarea.fecha"
                
                >
            </div>
            <div>
                <label class="labeldiv font-bold text-green-900 uppercase">
                    Asunto a la Actividad a realizar
                </label>
                <textarea name="" id="" class="label-input w-full my-2 rounded-md px-2 py-1 h-20 placeholder:text-white-400" placeholder="Describa la actividad a realizar"
                v-model="tarea.asunto"
                ></textarea>
            </div>
            <input @submit="validar " type="submit" class=" block rounded-md bg-orange-200 w-full hover:bg-red-400 cursor-pointer h-10 uppercase font-bold">
        </form>
    </div>
        
</template>





<style>
    .formulario{
        margin: 10px 30px;
        padding: 20px 30px;
        background: rgb(240,200,228);
        background: radial-gradient(circle, rgba(240,200,228,1) 22%, rgba(233,168,228,1) 72%);
        border: 2px solid rgb(27, 128, 14);
    }
    .contenedor-formulario{
        width: 100%;
        display: flex;
        justify-content: center;
    }
    .labeldiv{
        display: block;
    }
    .label-input{
        
        border: 2px solid blue;
    }
</style>