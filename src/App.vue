<template>
  <div class="main-container">
    <Navbar />
    <RouterView />
  </div>
</template>

<script>
  import { RouterLink, RouterView } from 'vue-router'
  import Navbar from './components/Navbar.vue'
  import NotesView from './views/NotesView.vue'

  export default {
    components: {
      Navbar,
      NotesView
    },
    data(){
      return{
        backgroundImgSrc: "/img/Estrelas.png",
      }
    }
  }

</script>

<style>
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Nunito', sans-serif;;
  }

  body {
    background-color: #1B2A40;
    background-image: url("/img/Estrelas.png"); 
    background-attachment: fixed;
    background-size: cover;
  }

  .main-container{
    margin: 0 300px 0 300px;
    min-height: 100vh;
  }

  .btn-main {
    border: none;
    border-radius: 10px;
    background-color: #FA00FF;
    color:#1B2A40; 
    padding: 10px;
    cursor: pointer;
    transition: ease-in-out .2s;
  }

  .btn-main:hover{
    background-color: #f87afa;
  }

</style>
