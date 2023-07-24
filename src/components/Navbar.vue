<template>
    <nav id="nav-main">
        <RouterLink to="/">Anotações</RouterLink>
        <RouterLink to="/pedidos">Checklist</RouterLink>
        <ToggleButton />
    </nav>

</template>

<script>
    import ToggleButton from './ToggleButton.vue'

    export default {
        name: 'Navbar',
        components: {
            ToggleButton
        }
    }
</script>

<style scoped>
    #nav-main{
        margin: 30px 0px 30px 0px;
        padding: 2px;
        width: 100%;
        height: 8vh;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        gap: 30px;
    }

    a {
        text-decoration: none;
        color: #B675B7;
        transition: ease-in .3s;
    }

    a:hover{
        color: #d5b5d5;
    }

    
</style>
