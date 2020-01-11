<template>
  <div align="center">
    <h1 class="mt-10 mb-5">
      <slot />
    </h1>
  </div>
</template>

<style scoped>
h1 {
  position: relative;
  display: inline-block;
  padding: 0 55px;
  font-size: 2rem;
  font-family: 'Gloria Hallelujah', cursive !important;
}

h1:before,
h1:after {
  content: '';
  position: absolute;
  top: 50%;
  display: inline-block;
  width: 45px;
  height: 2px;
  border-top: solid 1px black;
  border-bottom: solid 1px black;
}

h1:before {
  left: 0;
}
h1:after {
  right: 0;
}
</style>
