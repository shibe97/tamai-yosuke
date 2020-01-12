<template>
  <v-container>
    <section>
      <v-row justify="center">
        <h2>Blog</h2>
      </v-row>
      <ul>
        <li v-for="content in contents" :key="content.id">
          <a :href="`/blog/${content.id}`">{{ content.title }}</a>
        </li>
      </ul>
    </section>
  </v-container>
</template>
<script>
import axios from 'axios'
export default {
  async asyncData({ params, error, payload }) {
    const limit = 10
    const { data } = await axios.get(
      `https://tamasuke.microcms.io/api/v1/blog?limit=${limit}`,
      {
        headers: {
          'X-API-KEY': '6cb11011-fa2f-4bd0-86b4-3fd32cc0c42a'
        }
      }
    )
    return data
  }
}
</script>
