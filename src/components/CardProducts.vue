<template>
    <div class='container'>
        <SingleCard v-for="character in charactersList"
            :image="character.card_images[0].image_url"
                                                         />
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
        width: 75%;
        height: 100%;
        background-color: white;
        margin: 0 auto;
    }
</style>