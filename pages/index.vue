<template>
  <section>
    <v-sheet color="#fafafa" height="100vh">
      <v-container fill-height fluid :px-12="$vuetify.breakpoint.mdAndUp">
        <v-col align="center">
          <v-img
            :src="require('@/assets/hero.svg')"
            max-height="550"
            max-width="600"
            style="transform: translate(-4%, -5%)"
          />

          <h1
            class="text-uppercase font-weight-bold mb-4"
            :class="[$vuetify.breakpoint.xsOnly ? 'display-1' : 'display-3']"
          >
            tamai-yosuke
          </h1>

          <div
            class="mb-12"
            :class="[
              $vuetify.breakpoint.xsOnly
                ? 'title'
                : 'display-1 font-weight-light'
            ]"
          >
            official website
          </div>

          <v-slide-x-transition appear>
            <!-- <v-btn large class="px-5" color="primary">
              Hire Me -->
            <v-icon x-large>mdi-arrow-down-drop-circle-outline</v-icon>
            <!-- </v-btn> -->
          </v-slide-x-transition>
        </v-col>
      </v-container>
    </v-sheet>
  </section>
</template>
