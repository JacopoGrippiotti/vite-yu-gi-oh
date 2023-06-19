<template>
    <main>
        <div class="container">
        </div>
    </main>
    
</template>
<script>
export default {
    name:'AppMain'
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    main{
        background-color: orange;
        display: flex;
        padding-top: 80px;
        div.container{
        width: 80%;
        height: 1200px;
        background-color: white;
        margin: 0 auto;

    }
    }
    
</style>