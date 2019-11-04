<template>
  <v-sheet color="#fafafa" height="100vh">
    <v-container fill-height fluid>
      <v-col align="center">
        <v-img
          :src="require('@/assets/hero.svg')"
          style="transform: translate(-4%, 0%)"
          max-height="550"
          max-width="600"
        />

        <h1 class="text-uppercase toptitle mt-10">
          tamai-yosuke
        </h1>
        <v-icon
          class="pt-3"
          size="60px"
          @click="$vuetify.goTo('#news', options)"
          >mdi-chevron-down</v-icon
        >
        <!-- <v-slide-x-transition appear> -->
        <!-- <v-btn large class="px-5" color="primary">
              Hire Me -->
        <!-- <v-icon x-large>mdi-arrow-down-outline</v-icon> -->
        <!-- </v-btn> -->
        <!-- </v-slide-x-transition> -->
      </v-col>
    </v-container>
  </v-sheet>
</template>
<script>
export default {
  // data() {
  //   return {
  //     toptitle: '',
  //     topsubtitle: ''
  //   }
  // },
  computed: {
    options() {
      return {
        duration: 500,
        offset: 20
      }
    }
  }
  // mounted() {
  //   return (
  //     (this.toptitle = [
  //       this.$vuetify.breakpoint.xsOnly ? 'display-1' : 'display-3'
  //     ]),
  //     (this.topsubtitle = [
  //       this.$vuetify.breakpoint.xsOnly
  //         ? 'title'
  //         : 'display-1 font-weight-light'
  //     ])
  //   )
  // }
}
</script>
<style scoped>
.toptitle {
  font-family: 'Gloria Hallelujah', cursive !important;
  font-size: 2rem;
}
</style>
