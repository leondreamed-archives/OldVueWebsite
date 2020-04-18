<template lang="pug">
  v-app
    v-card.overflow-hidden(height="100vh")
      TheAppBar
      v-sheet#content-container.overflow-y-auto(min-height="100vh")
        v-content
          nuxt
        TheAppFooter
</template>

<script>
import TheAppBar from '~/components/TheAppBar.vue';
import TheAppFooter from '~/components/TheAppFooter.vue';

export default {
  components: { TheAppBar, TheAppFooter }
};
</script>

<style lang="sass">
$footer-height: 100px

*
  box-sizing: border-box

html, body
  overflow: auto
  height: 100%

#content-container
  display: flex
  flex-direction: column
  height: 100vh

.v-footer
  margin-top: auto
</style>
