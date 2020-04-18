<template lang="pug">
  .home-container
    .home-jumbotron
      v-card.ma-6(elevation=24)
        v-card-title Hi, I'm Leon, an aspiring ultralearner!
        v-card-subtitle This site in a work in progress...
        v-card-text.
          On my site, you can find articles I've written about my learning
          experiences, or projects I've built that helped make my life more
          efficient.
</template>

<script>
export default {};
</script>

<style scoped lang="sass">
.home-jumbotron
  display: flex
  align-items: center
  justify-content: center
  position: relative
  width: 100%
.v-card
  background-color: rgba(255, 255, 255, 0.9)
</style>
