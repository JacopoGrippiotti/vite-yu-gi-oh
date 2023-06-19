<template>
    <div class="card">
        <div class="img-wrapper">
            <img :src="image" alt="">
        </div>
        
        <div class="card-title">
            {{ name }}
        </div>
        <div class="card-type">
            {{ type }}
        </div>
    </div>
</template>

<script>
export default {
    name:'SingleCard',
    data() {
        return {
            
        }
    },
    props:{
        image: String,
        name: String,
        type:String
    }
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    div.card{
        width: calc((100% / 5) - 30px);
        background-color: orange;
        margin-top: 20px;
        display: flex;
        flex-direction: column;
        align-content: space-between;
        text-align: center;

        div.card-title{
            color: white;
            padding: 10px 0px;
            font-size: 1rem;
            font-weight: 600;
        }

        div.card-type{
            margin: 10px 0px;
        }
        div.img-wrapper{
            width: 100%;
            

            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: top;
            }
        }
    }
</style>