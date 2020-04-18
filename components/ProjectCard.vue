<template lang="pug">
  v-card
    v-img(:src="thumbnail")
    v-card-title {{ name }}
    v-card-subtitle {{ slogan }}
    v-card-text {{ description }}
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    },
    slogan: {
      type: String,
      default: ''
    },
    thumbnail: {
      type: String,
      default: ''
    },
    description: {
      type: String,
      default: ''
    }
  }
};
</script>
