<template>
    <div class="card">
        <div class="img-wrapper">
            <img :src="image" alt="">
        </div>
        
        <div class="card-title">
            adsdadsaad
        </div>
        <div class="card-type">
            
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
        image: String
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