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
import {store} from '../store';
export default {
    name:'CardProducts',
    components:{
        SingleCard
    },
    props:{
        charactersList:Array
    },
    data(){
        return{
            store,
            
        }
    },
    
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
        margin: 30px auto;
        padding-bottom: 30px;
    }
</style>