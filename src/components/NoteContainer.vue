<template>
  <div class="note-container">
    <note-selectors v-bind:notes="notes"/>
    <note-editor />
    <multi-select />
  </div>
</template>

<script>
  import NoteSelectors from "./NoteSelectors.vue"
  import NoteEditor from "./NoteEditor.vue"
  import MultiSelect from "./MultiSelect.vue"

  export default {
    name: 'note-container',
    components: {
      NoteSelectors,
      NoteEditor,
      MultiSelect
    },
    props: ['notes']
  }
</script>
