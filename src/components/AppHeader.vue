<template>
    <div class="title-container">
        <h1>Yu-Gi-Oh Api</h1>
    </div>
</template>

<script>
export default {
    name:'AppHeader'
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    div.title-container{
       background-color: white; 

        h1{
        font-size: 1.4rem;
        color: black;
    }
    }
    
</style>