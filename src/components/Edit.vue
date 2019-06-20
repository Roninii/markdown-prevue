<template lang="pug">
  v-card(
    height="90vh"
    width = '45vw'
    class=" pa-3 mt-3 elevation-5"
    )
    v-card-title 
      h2 Editor
    v-textarea(
      v-bind:text-content = "textContent"
      @input = "$emit('text-change', $event)"
      outline
      clearable = true
      height = '80vh'
      no-resize = true
      )
      
</template>

<script>
export default {
  name: "Edit",
  props: {
    textContent: {
      type: String,
      default: ""
    }
  }
};
</script>

<style scoped>
</style>

