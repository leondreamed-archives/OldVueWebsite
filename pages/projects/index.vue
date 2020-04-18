<template lang="pug">
  .project-cards
    ProjectCard(
      v-for="(project, index) in projects",
      :key="index",
      :name="project.name"
      :slogan="project.slogan"
      :thumbnail="project.thumbnail",
      :description="project.description"
    )

</template>

<script>
import ProjectCard from '~/components/ProjectCard.vue';

export default {
  components: { ProjectCard },
  data: () => ({
    projects: [
      {
        name: 'TimeTract',
        thumbnail: require('~/assets/project-thumbnails/timetract.png'),
        slogan: '⏱️ Keeping productivity accountable with competition.',
        description:
          'TimeTract uses the RescueTime API to keep users accountable through a ranking system where users compete to become the most productive.'
      },
      {
        name: 'Traduit',
        thumbnail: require('~/assets/project-thumbnails/traduit.png'),
        slogan: '🧠 When what gets translated gets memorized.',
        description:
          'Traduit is a Google Chrome extension that adds a small, unobtrusive button to the side of a translation. When this button is pressed, Traduit automatically adds this translation with the necessary context into your Anki deck.'
      },
      {
        name: 'Fulm',
        slogan: '⚡ The universal time-lapse screen recorder.'
      },
      {
        name: 'Paranoia',
        slogan: '👀 Accountability through observation.'
      }
    ]
  })
};
</script>

<style lang="sass" scoped>
.project-cards
  padding: 0 20px
  display: grid
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))
  grid-gap: 1rem
</style>
