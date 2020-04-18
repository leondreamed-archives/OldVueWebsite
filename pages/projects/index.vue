<template lang="pug">
  .px-8.pt-4
    h1.display-2.font-weight-bold.mb-4 Projects
    .project-cards
      BaseCard(
        v-for="(project, index) in projects",
        :key="index",
        type="projects"
        :title="project.title"
        :name="project.name"
        :slogan="project.slogan"
        :thumbnail="project.thumbnail",
        :description="project.description"
      )
</template>

<script>
import projects from '~/data/projects';

export default {
  data: () => ({
    projects
  })
};
</script>

<style scoped lang="sass">
.project-cards
  display: grid
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))
  grid-gap: 1rem
</style>
