<template>
  <v-app-bar app flat color="#fafafa">
    tamai-yosuke.com
    <v-spacer />
    <template v-if="$vuetify.breakpoint.mdAndUp">
      <v-btn
        v-for="(item, i) in items"
        :key="i"
        :to="item.to"
        class="text-capitalize subtitle-1 mx-1"
        text
        x-large
      >
        <span v-text="item.text" />
      </v-btn>
    </template>
    <v-menu v-else>
      <template v-slot:activator="{ on }">
        <v-btn icon v-on="on">
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </template>
      <v-card dark>
        <v-list color="transparent">
          <v-list-item v-for="(item, i) in items" :key="i" :to="item.to">
            <v-list-item-title v-text="item.text" />
          </v-list-item>
        </v-list>
      </v-card>
    </v-menu>
  </v-app-bar>
</template>

<script>
// Utilities
// import { mapMutations } from 'vuex'

export default {
  data: () => ({
    isScrolling: false,
    items: [
      {
        to: '/',
        text: 'Home'
      },
      {
        to: '/news',
        text: 'News'
      },
      {
        to: '/profile',
        text: 'Profile'
      },
      {
        to: '/contact',
        text: 'Contact'
      },
      {
        to: '/more',
        text: 'More'
      }
    ]
  }),

  methods: {
    // ...mapMutations(['toggleDrawer']),
    onScroll() {
      this.isScrolling =
        (window.pageYOffset || document.documentElement.scrollTop || 0) > 20
    }
  }
}
</script>
