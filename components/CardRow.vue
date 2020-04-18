<template lang="pug">
  h1.display-2.font-weight-bold {{ title }}
    .projects.d-flex
      BaseCard.mr-8.my-4(
        v-for="(card, index) of cards"
        :key="index"
        :type="type"
        :name="card.name"
        :title="card.title"
        :slogan="card.slogan"
        :thumbnail="card.thumbnail",
      )
    slot(name="button")
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    type: {
      type: String,
      required: true
    },
    cards: {
      type: Array,
      required: true
    }
  }
};
</script>
