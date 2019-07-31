<template>
    <div>
        <h1 v-if="show">{{title}}</h1>
        <button @click="showOrHide"> Mostrar/Ocultar</button>
        {{$props}}
    </div>
    
</template>
<script>
export default {
    data(){
        return {
            
        }
    },
    props:{
        show:{
            type:Boolean,
            required: true,
            default: false
        },
        title: {
            type: String,
            required: true,
            default: "No hay datos"}
    },
    methods:{
        showOrHide(){
            this.$emit("changeShow", !this.show)
        }
    }
   
}
</script>


