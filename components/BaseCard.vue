<template lang="pug">
  v-card(elevation="5", :to="`/${type}/${name}`")
    v-img(:src="thumbnail")
    v-card-title {{ title }}
    v-card-subtitle {{ slogan }}
    v-card-text(v-if="description") {{ description }}
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    },
    title: {
      type: String,
      default: ''
    },
    slogan: {
      type: String,
      default: ''
    },
    thumbnail: {
      type: String,
      default: require('~/assets/project-thumbnails/default.png')
    },
    type: {
      type: String,
      required: true
    },
    description: {
      type: String,
      default: ''
    }
  }
};
</script>
