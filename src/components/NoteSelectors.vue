<template>
  <div class="note-selectors">
    <note-selector
      v-for="note in notes"
      v-bind:key="note.id"
      v-bind:note="note"
      v-bind:selectedNoteId="selectedNoteId"
      v-on:selectNote="setSelectNote"
    />
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector.vue"

export default {
  name: 'note-selectors',
  components: {
    NoteSelector
  },
  data: function() {
    return {

      selectedNoteId: 3
    }
  },
  methods: {
    setSelectNote: function(noteId) {
      console.log(noteId);
      this.selectedNoteId = noteId;
    }
  },
  props: ['notes']
}

</script>
