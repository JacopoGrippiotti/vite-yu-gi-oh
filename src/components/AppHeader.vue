<template>
    <header>
        <h1>Yu-Gi-Oh Api</h1>
    </header>
</template>

<script>
export default {
    name:'AppHeader'
}
</script>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as*;
    @use '../styles/partials/variables' as*;

    header{
       background-color: white; 
       height: 60px;
       display:flex;
       align-items: center;
        
       h1{
        font-size: 2rem;
        color: black;
        margin-left: 70px;
        font-weight: normal;
    }
    }
    
</style>