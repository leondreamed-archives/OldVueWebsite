<template lang="pug">
  .px-8.pt-4
    h1.display-2.font-weight-bold.mb-4 Articles
    .article-cards
      BaseCard(
        v-for="(article, index) in articles",
        :key="index",
        type="articles"
        :title="article.title"
        :name="article.name"
        :slogan="article.slogan"
        :thumbnail="article.thumbnail",
        :description="article.description"
      )
</template>

<script>
import articles from '~/data/articles';

export default {
  data: () => ({
    articles
  })
};
</script>

<style scoped lang="sass">
.article-cards
  display: grid
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))
  grid-gap: 1rem
</style>
