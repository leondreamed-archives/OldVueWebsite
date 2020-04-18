<template lang="pug">
  .ma-6
    v-btn.mb-6(to="/articles", exact)
      v-icon mdi-chevron-left
      | All Articles
    div(v-html="content")
</template>

<script>
export default {
  data: () => ({
    content: ''
  }),
  async created() {
    const { default: content } = await import(
      `~/content/articles/${this.$route.params.name}.md`
    );
    this.content = content;
  }
};
</script>

<style scoped lang="sass">
.project-cards
  display: grid
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))
  grid-gap: 1rem
</style>
