<template>
  <div id="app">
    <NavBar></NavBar>
    <router-view/>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
export default {
  components: {
    NavBar
  }
}
</script>

<style lang="scss">
html,
body {
  background-color: #f7f7f7 !important;
  color: #777777;
  font-size: 14px;
  font-family: Lato, sans-serif;
  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    font-family: 'Roboto Condensed', sans-serif;
    font-weight: 500;
  }
  a {
    color: #f5bb00;
    background-color: transparent;
  }
}
</style>
