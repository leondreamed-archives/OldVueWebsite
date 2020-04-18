<template lang="pug">
  v-app-bar(
    absolute
    color="white"
    elevate-on-scroll
    scroll-target="#content-container"
    app
  )
    v-btn(text, to="/") Home
    v-btn(text, to="/projects") Projects

</template>
