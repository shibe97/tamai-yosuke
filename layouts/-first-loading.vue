<template>
  <div :class="{ 'is-finish': dataLoadFinish }" class="loading">
    <v-img
      :src="require('@/assets/logo.png')"
      max-height="70px"
      width="auto"
      contain
    />
    <p>loading...</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dataLoadFinish: false
    }
  },
  mounted() {
    window.addEventListener('load', () => {
      this.dataLoadFinish = true
    })
  }
}
</script>

<style lang="scss" scoped>
.loading {
  position: fixed;
  z-index: 3;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100vw;
  height: 100vh;
  color: black;
  &.is-finish {
    transition: opacity 1s, z-index 0s 1.01s;
    opacity: 0;
    z-index: -1;
  }
}
</style>
