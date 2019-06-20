<template lang="pug">
  v-app
    v-container(fluid class="pa-0")
      v-layout(
        wrap = true
        justify-space-around = true
      )
        Edit(
          :text-content="textContent"
          @text-change="textContent = $event"
        )
        Preview(
          :preview="markdown"
        )
      v-btn Cheat Sheet
</template>

<script>
import Edit from "./components/Edit";
import Preview from "./components/Preview";

const dummyText = "Hello World";

export default {
  name: "App",
  data() {
    return {
      textContent: null,
      demo: dummyText
    };
  },
  components: {
    Edit,
    Preview
  },
  computed: {
    markdown() {
      if (this.textContent) {
        return marked(this.textContent, {
          // marked options
          headerIds: false
        });
      }
    }
  }
};
</script>

<style>
</style>
