<template>
  <div class="sidebar">
    <div class="sidebar-wrapper">
      <LatestPosts></LatestPosts>
      <Categories></Categories>
      <Tags></Tags>
    </div>
  </div>
</template>

<script>
import LatestPosts from '@/components/sidebar_widgets/LatestPosts.vue'
import Categories from '@/components/sidebar_widgets/Categories.vue'
import Tags from '@/components/sidebar_widgets/Tags.vue'

export default {
  name: 'sidebar',
  components: {
    LatestPosts,
    Categories,
    Tags
  }
}
</script>

<style lang="scss" scoped>
.sidebar {
  background-color: #fff;
  padding: 20px;
  .sidebar-wrapper {
    .widget {
      clear: both;
      margin-bottom: 40px;
    }
  }
}
</style>
