<template>
  <v-container class="px-5">
    <section>
      <v-row justify="center">
        <h2>Blog</h2>
      </v-row>
      <span class="article_date mt-3"
        ><v-icon>mdi-av-timer</v-icon>{{ createdAt }}</span
      >
      <h1 class="mt-0">{{ blogtitle }}</h1>
      <div class="article_content" v-html="blogcontent" />
      <div><a href="./">ブログ記事一覧へ</a></div>
    </section>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    blogtitle: '',
    blogcontent: '',
    createdAt: ''
  }),
  mounted() {
    // URLパラメータからidを取得
    const id = this.$route.params.id
    // microCMSからコンテンツを取得
    fetch(`https://tamasuke.microcms.io/api/v1/blog/${id}`, {
      headers: {
        'X-API-KEY': '6cb11011-fa2f-4bd0-86b4-3fd32cc0c42a'
      }
    })
      .then((result) => result.json())
      .then((json) => {
        this.blogtitle = json.title
        this.blogcontent = json.content
        this.createdAt = json.createdAt.slice(0, 10)
      })
  }
}
</script>
<style scoped>
>>> .article_content img {
  width: 100%;
  height: auto;
}
</style>
