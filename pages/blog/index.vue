<template>
  <v-container>
    <section>
      <v-row justify="center">
        <h2>Blog</h2>
      </v-row>
      <ul id="blogs"></ul>
    </section>
  </v-container>
</template>
<script>
export default {
  mounted() {
    fetch('https://tamasuke.microcms.io/api/v1/blog', {
      headers: {
        'X-API-KEY': '6cb11011-fa2f-4bd0-86b4-3fd32cc0c42a'
      }
    })
      .then((res) => res.json())
      .then((json) => {
        // 画面表示
        const list = json.contents
          .map(
            (content) =>
              `<li><a href="/blog/${content.id}">${content.title}</a></li>`
          )
          .join('\n')
        document.getElementById('blogs').innerHTML = list
      })
  }
}
</script>
