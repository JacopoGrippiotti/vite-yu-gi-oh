<template>
    <div class='container'>
        <SingleCard v-for="character in charactersList"
            :image="character.card_images[0].image_url"
            :name="character.name"                      
            :type="character.type"                                          />
    </div>
</template>
<script>
import SingleCard from './SingleCard.vue';
import axios from 'axios';
import {store} from '../store';
export default {
    name:'CardProducts',
    components:{
        SingleCard
    },
    data(){
        return{
            apiUrl:'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
            charactersList:[],
            store
        }
    },
    created(){
        axios.get(this.apiUrl)
        .then((response) => {
            console.log(response.data.data)
            this.charactersList = response.data.data
        }) 
        .catch(function (error){
            console.log(error)
        })
        
    }
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    div.container{
        @include flex(row,space-evenly,wrap);
        width: 85%;
        height: 100%;
        background-color: white;
        margin: 60px auto;
        padding-bottom: 30px;
    }
</style>