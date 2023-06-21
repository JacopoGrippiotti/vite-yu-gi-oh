<template>
    <main>
        <DropdownFilter @changedArchetype="callApi"/>
        <CardProducts
         :charactersList="charactersList"/>
    </main>
    
</template>
<script>
import CardProducts from './CardProducts.vue';
import DropdownFilter from './DropdownFilter.vue';
import axios from 'axios';
export default {
    name:'AppMain',
    components:{
        CardProducts,
        DropdownFilter
    },
    data(){
        return{
            apiUrl:'https://db.ygoprodeck.com/api/v7/cardinfo.php?',
            response:[],
            charactersList:[]
        }
    },
    methods:{
        callApi(needle){
            axios.get(this.apiUrl ,{
                params:{
                    num:20,
                    offset:0,
                    archetype:needle
                }
            })
        .then((response) => {
            this.response = response
            this.charactersList = response.data.data
        }) 
        .catch(function (error){
            console.log(error)
        })
        }
    },
    created(){
       this.callApi()
    }
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    main{
        background-color: orange;
        display: flex;
        flex-direction: column;
    }
    
</style>