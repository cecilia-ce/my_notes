<template>
    <div class="note-container">
        <div class="form-header">
            <h1>MINHAS ANOTAÇÕES</h1>
            <button class="btn-main">Excluir tudo</button>
            <button class="btn-main" @click="createNote($event)">Salvar</button>
        </div>
        <textarea id="text-area-note" placeholder="Digite sua anotação" v-model="text"></textarea>
    </div>
</template>

<script>
import NotesViewVue from '../views/NotesView.vue';
export default{
    name: 'NoteForm',
    data(){
        text: null

    },
    methods: {
        async createNote(e){
            e.preventDefault();
            const data = {
                text: this.text  
            }; 
            
            const dataJson = JSON.stringify(data);

            const req = await fetch('http://localhost:3000/notes', {
                method: "POST",
                headers: {"content-type": "application/json"}, 
                body: dataJson
            });

            const res = await req.json();

        }
    },
    
    
}
</script>

<style scoped>
    .note-container{
        border: 3px solid #FA00FF;
        border-radius: 10px;
        padding: 10px;
        color:#FA00FF;
    }

    .form-header{
        width: 100%;
        display: flex;
        justify-content: end;
        gap: 10px;
    }
    
    .form-header h1 {
        font-size: 20px;
        margin: auto;
        margin-left: 0;
    }

    textarea {
        resize: none;
        border: none;
        width: 100%;
        height: 20vh;
        margin-top: 20px;
        background: none;
        color: #FA00FF;
    }

    textarea::placeholder {
        color: #923F93;
    }

    textarea:focus {
        resize: none;
        border: none;
        outline: 0;
    }
    
</style>
