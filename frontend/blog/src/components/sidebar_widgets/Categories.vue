<template>
  <div class="widget cate">
    <h2>Categories</h2>
    <div class="widget-content list-cates">
      <ul>
        <li v-for="item in [1,2,3,4,5]" :key="item">
          <a href>Vue.js</a>
          <span>( 2 )</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Categories'
}
</script>

<style lang="scss" scoped>
.sidebar {
  background-color: #fff;
  padding: 20px;
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    margin: 0 0 0 0px;
    padding: 0 0 0px;
    text-transform: capitalize;
    display: list-item;
    text-align: -webkit-match-parent;
  }
  .sidebar-wrapper {
    .widget {
      clear: both;
      margin-bottom: 40px;
      h2 {
        padding: 0 0 15px;
        line-height: 1;
        font-size: 14px;
        text-transform: uppercase;
        color: #50514f;
        border-bottom: 1px solid #f4f4f4;
        position: relative;
        text-align: left;
        margin-block-start: 0.83em;
        margin-block-end: 0.83em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
        display: block;
        margin: 0;
        &:after {
          position: absolute;
          content: ' ';
          z-index: 1;
          bottom: -1px;
          left: 0;
          width: 100px;
          height: 1px;
          background-color: #f5bb00;
        }
      }
      .list-cates {
        ul {
          list-style: none;
          padding-top: 20px !important;
          margin: 0;
          padding: 0;
          li {
            font-size: 14px;
            display: block;
            padding: 15px 0 !important;
            border-bottom: 1px solid #f4f4f4;
            margin: 0 !important;
            position: relative;
            a {
              color: #999;
              display: block;
              text-decoration: none;
            }
            span {
              height: 30px;
              padding: 0 10px;
              line-height: 30px;
              background-color: #f5bb00;
              color: #fff;
              position: absolute;
              right: 0;
              top: 10px;
              font-weight: 700;
              -webkit-transition: background-color ease 0.2s;
              -moz-transition: background-color ease 0.2s;
              -o-transition: background-color ease 0.2s;
              transition: background-color ease 0.2s;
            }
          }
        }
      }
    }
  }
}
</style>
