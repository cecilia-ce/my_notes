<template>
    <NoteForm />
    <NoteCard />
    
</template>

<script>
import NoteForm from '../components/NoteForm.vue'
import NoteCard from '../components/NoteCard.vue'

export default{
    name: 'NotesView',
    components: {
        NoteForm,
        NoteCard
    }
   
}
</script>

<style scoped>

</style>
