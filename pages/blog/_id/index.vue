<template>
  <v-container class="px-5">
    <section>
      <v-row justify="center">
        <h2>Blog</h2>
      </v-row>
      <span class="article_date mt-3">
        <v-icon>mdi-av-timer</v-icon>
        {{ createdAt }}
      </span>
      <h1 class="mt-0">{{ blogtitle }}</h1>
      <div class="article_content" v-html="blogcontent" />
      <div>
        <a href="./">ブログ記事一覧へ</a>
      </div>
    </section>
  </v-container>
</template>
<script>
import axios from 'axios'
export default {
  data: () => ({
    blogtitle: '',
    blogcontent: '',
    createdAt: ''
  }),

  async asyncData({ params, error, payload }) {
    let data
    if (payload !== undefined) {
      data = payload
    } else {
      const result = await axios.get(
        `https://tamasuke.microcms.io/api/v1/blog/${params.id}`,
        {
          headers: {
            'X-API-KEY': '6cb11011-fa2f-4bd0-86b4-3fd32cc0c42a'
          }
        }
      )
      data = result.data
    }
    return {
      blogtitle: data.title,
      blogcontent: data.content,
      createdAt: data.createdAt.slice(0, 10)
    }
  }
}
</script>
<style scoped>
>>> .article_content img {
  width: 100%;
  height: auto;
}
</style>
