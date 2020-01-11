<template>
  <v-app>
    <hero />
    <live id="news" />
    <member />
    <contact id="contact" />
  </v-app>
</template>
<script>
export default {
  components: {
    Hero: () => import('@/components/Hero.vue'),
    Live: () => import('@/components/Live.vue'),
    Member: () => import('@/components/Member.vue'),
    Contact: () => import('@/components/Contact.vue')
  }
}
</script>
