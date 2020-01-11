<template>
  <v-col align="center">
    <div class="mb-7">
      <h2>members</h2>

      <v-card class="mx-auto" max-width="800" tile flat>
        <v-img :src="require('@/assets/images/member.jpg')" />
        <v-card-text class="text--primary title">
          <p>vo/gt たまいやすゆき</p>
          <p>vo/per よーすけ</p>
          <v-btn flat elevation="0" to="/profile">Read More</v-btn>
        </v-card-text>
      </v-card>
    </div>
  </v-col>
</template>
