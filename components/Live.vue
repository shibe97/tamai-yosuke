<template>
  <v-col align="center">
    <div class="news-box mb-7">
      <h2>live schedule</h2>
      <p
        id="content"
        class="pt-2 px-3"
        align="left"
        :class="$vuetify.breakpoint.smAndUp ? 'headline' : 'body-1'"
      />
    </div>
    <v-row justify="center">
      <v-btn text to="/line"
        ><span style="color: green;">LINE</span>で最新情報をお届けします</v-btn
      >
    </v-row>
  </v-col>
</template>
<script>
export default {
  mounted() {
    fetch('https://tamasuke.microcms.io/api/v1/live/De7Ak6zM0', {
      headers: {
        'X-API-KEY': '6cb11011-fa2f-4bd0-86b4-3fd32cc0c42a'
      }
    })
      .then((res) => res.json())
      .then((json) => {
        document.getElementById('content').innerHTML = json.contents
      })
  }
}
</script>
<style scoped>
.news-box {
  max-width: 500px;
}
.news-box p {
  font-size: 1.1em;
  line-height: 1.5em;
}
</style>
