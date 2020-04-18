<template lang="pug">
  .ma-6
    v-btn.mb-6(to="/projects", exact)
      v-icon mdi-chevron-left
      | All Projects
    div(v-html="content")
</template>

<script>
export default {
  data: () => ({
    content: ''
  }),
  async created() {
    const { default: content } = await import(
      `~/content/projects/${this.$route.params.name}.md`
    );
    this.content = content;
  }
};
</script>
