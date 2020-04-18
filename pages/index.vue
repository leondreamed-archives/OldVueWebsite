<template lang="pug">
  .home-container
    HomeJumbotron
    .pa-8.home-content-container.mx-auto.overflow-hidden
      CardRow.mb-3(
        :cards="articles"
        title="Recent Articles"
        type="articles"
      )
        template(v-slot:button)
          v-btn(to="/articles") View All Articles
      CardRow.mt-3(
        :cards="projects"
        title="Recent Projects"
        type="projects"
      )
        template(v-slot:button)
          v-btn(to="/projects") View All Projects
</template>

<script>
import HomeJumbotron from '~/components/HomeJumbotron.vue';
import CardRow from '~/components/CardRow.vue';
import projects from '~/data/projects';
import articles from '~/data/articles';

export default {
  components: { HomeJumbotron, CardRow },
  data: () => ({
    projects: projects.slice(0, 4),
    articles: articles.slice(0, 4)
  }),
  head() {
    return {
      title: "Leon Si (leonzalion)'s personal website.",
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            "Hi, I'm Leon, an aspiring ultralearner. Here, you can find articles I've written about my learning experiences and some projects I've created to make my life more efficient."
        }
      ]
    };
  }
};
</script>

<style scoped lang="sass">
.v-carousel
  margin: 50px
  width: 600px
.home-content-container
  max-width: 1440px
</style>
