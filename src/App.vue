<template>
<div>
    <header-nav :title="title" 
                :show="show" 
                @changeShow="changeStateText"></header-nav>
    <header-nav :title="title" 
                :show="show" 
                @changeShow="changeStateText"></header-nav>            
                {{$data}}
</div> 
</template>
<script>
import HeaderNav from './components/Header.vue'
export default {

    data(){
        return {
            show: true,
            title: "Titulo del padre"
        }
    },
    methods: {
        changeStateText(state){
            this.show= state
        }
    },
    computed: {

    },
    components:{
        HeaderNav
    }
}
</script>
<style>

</style>

