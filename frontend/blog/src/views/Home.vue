<template>
  <b-container fluid>
    <b-row>
      <b-col>
        <AboutMeCard></AboutMeCard>
      </b-col>
    </b-row>
    <b-row class="content">
      <!-- articlelist -->
      <b-col cols="md-8">
        <AboutMeCard></AboutMeCard>
      </b-col>
      <!-- sidebar -->
      <b-col cols="md-4">
        <SideBar></SideBar>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
// @ is an alias to /src
import AboutMeCard from '@/components/AboutMeCard.vue'
import SideBar from '@/components/SideBar.vue'

export default {
  name: 'Home',
  components: {
    AboutMeCard,
    SideBar
  }
}
</script>

<style lang="scss" scoped>
.container-fluid {
  padding: 0;
  margin: 0;
  .content {
    margin: 40px;
  }
}
</style>
