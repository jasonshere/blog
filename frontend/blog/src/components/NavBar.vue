<template>
  <div>
    <!-- NarBar -->
    <b-navbar toggleable="md" type="dark" variant="info" fixed="top" sticky>
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar-brand to="#">
        <img class="brand_avatar d-inline-block align-top" :src="avatar" alt="BV">
        Jason's Note
      </b-navbar-brand>

      <b-collapse is-nav id="nav_collapse">
        <b-navbar-nav class="ml-auto">
          <b-nav-item to="/home" active>Home</b-nav-item>
          <b-nav-item-dropdown text="Categories">
            <b-dropdown-item to="#">EN</b-dropdown-item>
            <b-dropdown-item to="#">中文</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
        <!-- Right aligned nav items -->
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
import avatar from '@/assets/imgs/avatar.jpeg'
export default {
  name: 'NavBar',
  data () {
    return {
      progress: 100,
      max: 100,
      avatar: avatar
    }
  }
}
</script>

<style lang="scss" scoped>
html,
body {
  img.brand_avatar {
    border-radius: 50%;
    margin-right: 10px;
    width: 30px;
  }
}
</style>
