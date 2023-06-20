<template>
    <div class="container">
        <select class="dropdown-menu" @change="ciao" v-model="selectedArchetype">
          <option v-for="archetype in archetypeList" :value="archetype" >{{ archetype }}</option>
        </select>
    </div>
    
</template>
<script>
import axios from 'axios';
export default {
    name:'DropdownFilter',
    data(){
        return{
            apiUrl:'https://db.ygoprodeck.com/api/v7/archetypes.php',
            archetypeList:[],
            selectedArchetype:""
        }
    },
    methods:{
       ciao(){
        console.log(this.selectedArchetype)
       }
    },
    created(){
        axios.get(this.apiUrl)
        .then((response) => {

            for (let i=0; i<3; i++){
                this.archetypeList.push(response.data[i].archetype_name)
            }
            

            
            console.log(this.archetypeList)
        })
    }
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    div.container{
        width: 85%;
        margin: 0 auto;
        div.dropdown-menu{
        background-color: white;
        border: 1px solid black;
        width: 120px;
        margin-top: 30px;
    }

    }
    
</style>