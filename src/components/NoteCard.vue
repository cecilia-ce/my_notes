<template>
    <div class="note-container">
        <div class="card-header">
            <button class="btn-delete">Excluir</button>
        </div>
        <p id="note-text" class="note-text">{{ noteText }}</p>
    </div>
</template>

<script>
export default{
    name: 'NoteCard',
    data(){
        return{
            
        }
    },
    props: {
        noteText: String
    }
    
    
}
</script>

<style scoped>
    .note-container{
        margin-top: 30px;
        border: 3px solid #FA00FF;
        border-radius: 10px;
        padding: 10px;
        color:#F9D8FF;
        background-color: rgba(250,0,255,0.2); 
        
    }

    .card-header{
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

    .btn-delete{
        border: none;
        border-radius: 15px;
        background-color: #FA00FF;
        color:#1B2A40; 
        padding: 5px;
        font-size: 12px;
        cursor: pointer;
        transition: ease-in-out .2s;
    }

    .btn-delete:hover{
        background-color: #f87afa;
    }

    p {
        width: 100%;
        word-wrap: break-word;
    }   
    
</style>
