<template>
    <NoteForm />
    <NoteCard v-for="note in notes" :key="note.id" :noteText="note.text" />
    
</template>

<script>
import NoteForm from '../components/NoteForm.vue'
import NoteCard from '../components/NoteCard.vue'

export default{
    name: 'NotesView',
    data() {
        return {
            notes: null
        }
    },
    components: {
        NoteForm,
        NoteCard
    },
    methods: {
        async getNotes(){
            const req = await fetch('http://localhost:3000/notes');
            const data = await req.json();
            this.notes = data;
        }
    },
    mounted (){
        this.getNotes()
    }
   
}
</script>

<style scoped>

</style>
