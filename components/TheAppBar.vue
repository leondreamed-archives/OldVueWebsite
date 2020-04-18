<template lang="pug">
  v-app-bar(
    absolute
    color="white"
    elevate-on-scroll
    scroll-target="#content-container"
    app
  )
    v-btn(
      v-for="(tab, index) of tabs"
      :to="tab.route"
      :key="index"
      height="100%"
      text
    ) {{ tab.name }}
    v-spacer
    v-btn.mr-2(to="/register") Register
    v-btn(to="/login") Login
</template>

<script>
export default {
  data: () => ({
    tabs: [
      {
        name: 'Home',
        route: '/'
      },
      {
        name: 'About',
        route: '/about'
      },
      {
        name: 'Projects',
        route: '/projects'
      },
      {
        name: 'Paranoia',
        route: '/paranoia'
      }
    ]
  })
};
</script>
