<template lang="pug">
  v-card(
    width = '45vw'
    class=" pa-3 mt-3 elevation-5"
  )
    v-card-title
     h2 Prevue
    v-divider
    v-card-text(v-html="preview")
  
</template>

<script>
export default {
  name: "Preview",
  props: {
    preview: {
      type: String,
      default: ""
    }
  }
};
</script>

<style scoped>
</style>

