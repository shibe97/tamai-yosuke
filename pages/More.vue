<template>
  <v-container>
    <section>
      <h2>More</h2>
    </section>
    <v-col cols="12" align="center">
      <v-card flat title max-width="900" min-height="400">
        <v-tabs centered show-arrows>
          <v-tab v-for="(category, i) in categories" :key="i">
            <span class="title" v-text="category" />
          </v-tab>

          <v-tab-item>
            <v-card flat title>
              <v-card-text class="vcontent my-5">
                <v-col align="center">
                  T
                </v-col>
              </v-card-text>
            </v-card>
          </v-tab-item>
          <v-tab-item>
            <v-card flat tile>
              <v-card-text class="my-5">
                <v-col align="center">
                  A
                </v-col>
              </v-card-text>
            </v-card>
          </v-tab-item>
          <v-tab-item class="vcontent">
            <v-card flat title class="vcontent">
              <v-card-text class="vcontent my-5">
                <v-col align="center">
                  M
                </v-col>
              </v-card-text>
            </v-card>
          </v-tab-item>
          <v-tab-item class="vcontent">
            <v-card flat title class="vcontent">
              <v-card-text class="vcontent my-5">
                <v-col align="center">
                  I
                </v-col>
              </v-card-text>
            </v-card>
          </v-tab-item>
        </v-tabs>
      </v-card>
    </v-col>
  </v-container>
</template>
<script>
export default {
  components: {},
  data: () => ({
    categories: ['Music', 'Media', 'Gallery']
  })
}
</script>
