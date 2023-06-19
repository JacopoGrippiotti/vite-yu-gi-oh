<template>
    <main>
        <CardProducts/>
    </main>
    
</template>
<script>
import CardProducts from './CardProducts.vue';
export default {
    name:'AppMain',
    components:{
        CardProducts
    }
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    main{
        background-color: orange;
        display: flex;
        padding-top: 80px;
        height: 1800px;
    }
    
</style>