<template>
    <div class="container">
        <div class="dropdown-menu">
          ciao
        </div>
    </div>
    
</template>
<script>
export default {
    name:'DropdownFilter',
    data(){
        return{

        }
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