<template>
  <v-app>
    <hero />
    <news id="news" />
  </v-app>
</template>
<script>
export default {
  components: {
    Hero: () => import('@/components/Hero.vue'),
    News: () => import('@/components/News.vue')
  }
}
</script>
