<template>
  <v-app>
    <core-header />
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <core-footer />
  </v-app>
</template>
<script>
export default {
  components: {
    CoreHeader: () => import('@/components/core/Toolbar'),
    CoreFooter: () => import('@/components/core/Footer')
  }
}
</script>
