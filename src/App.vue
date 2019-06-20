<template lang="pug">
  v-app
    v-container(fluid class="pa-0")
      v-layout(
        wrap = true
        justify-space-around = true
      )
        Edit()
        Preview
</template>

<script>
import Edit from "./components/Edit";
import Preview from "./components/Preview";

export default {
  name: "App",
  components: {
    Edit,
    Preview
  }
};
</script>

<style>
</style>
