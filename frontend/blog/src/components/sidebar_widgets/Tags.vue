<template>
  <div class="widget tags">
    <h2>Tags</h2>
    <div class="widget-content list-tags">
      <span class="label-size" v-for="item in [1,2,3,4,5,6,7,8,9]" :key="item">
        <a href>Vue</a>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tags'
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
      .list-tags {
        padding-top: 10px;
        .label-size {
          display: inline-block;
          line-height: 30px;
          text-align: center;
          font-size: 14px;
          background-color: #f4f4f4;
          color: #999;
          margin: 0 5px 6px 0;
          border-radius: 2px;
          padding: 0 15px;
          -webkit-transition: background-color ease 0.2s, color ease 0.2s;
          -moz-transition: background-color ease 0.2s, color ease 0.2s;
          -o-transition: background-color ease 0.2s, color ease 0.2s;
          transition: background-color ease 0.2s, color ease 0.2s;
          a {
            color: #999;
            text-decoration: none;
            background-color: transparent;
          }
        }
      }
    }
  }
}
</style>
