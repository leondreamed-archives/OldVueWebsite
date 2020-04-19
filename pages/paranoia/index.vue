<template lang="pug">
  .pa-8
    p(v-html="description")
    v-sheet.pa-4(height="400", elevation="4")
      v-calendar(
        :now="today"
        :value="today"
        :events="events"
        type="week"
      )
    .text-center
      v-btn.ma-4(
        @click="takeScreenshot"
        :loading="loadingScreenshot"
      ) Take Screenshot
      v-img(v-if="screenshot" :src="screenshot")
      p(v-if="screenshotError") {{ screenshotError }}
</template>

<script>
import to from 'await-to-js';
import dateformat from 'dateformat';
import description from './description.md';

const serverUrl = 'https://paranoia-server.herokuapp.com';
export default {
  data: () => ({
    description,
    screenshot: '',
    today: dateformat('isoDate'),
    events: [],
    loadingScreenshot: false,
    screenshotError: ''
  }),
  methods: {
    async takeScreenshot() {
      this.loadingScreenshot = true;
      const [error, result] = await to(
        this.$axios.get(`${serverUrl}/leonzalion/screenshot`)
      );
      if (error) {
        this.screenshotError = 'Unable to get screenshot. Please try again.';
        return;
      }
      const { success, data, message } = result.data;
      if (!success) {
        this.screenshotError = message;
      } else {
        this.screenshot = data;
      }
      this.loadingScreenshot = false;
    }
  }
};
</script>
