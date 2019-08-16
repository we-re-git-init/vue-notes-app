<template>
  <div class="note-container">
    <note-selectors v-bind:notes="notes"/>
    <note-editor />
  </div>
</template>

<script>
  import NoteSelectors from "./NoteSelectors.vue"
  import NoteEditor from "./NoteEditor.vue"

  export default {
    name: 'note-container',
    components: {
      NoteSelectors,
      NoteEditor
    },
    props: ['notes']
  }
</script>
