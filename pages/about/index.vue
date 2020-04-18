<template lang="pug">
  .ma-6(v-html="about")
</template>

<script>
import about from './about.md';

export default {
  data: () => ({
    about
  })
};
</script>
