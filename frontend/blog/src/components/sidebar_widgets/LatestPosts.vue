<template>
  <div class="widget">
    <h2>Latest Posts</h2>
    <div class="widget-content latest-posts">
      <ul>
        <li v-for="item in [1,2,3,4,5]" :key="item">
          <div class="item">
            <div class="item-thumbnail-only">
              <div class="item-thumbnail">
                <a href>
                  <img
                    alt
                    border="0"
                    height="72"
                    src="https://2.bp.blogspot.com/-F_n7ri4nYYw/Vz9MxMksZgI/AAAAAAAAAJc/hODtwO32JVogQfSTZVzgKXGnvaqjz8RhgCLcB/s72-c/photo-1448518184296-a22facb4446f.jpg"
                    width="72"
                  >
                </a>
              </div>
              <div class="item-title">
                <a href>Jason's first version blog</a>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LatestPosts'
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
      .latest-posts {
        ul {
          list-style: none;
          padding-top: 20px !important;
          margin: 0;
          padding: 0;
          li {
            position: relative;
            padding-left: 0px;
            font-size: 14px;
            padding-bottom: 15px;
            margin-bottom: 15px;
            border-bottom: 1px solid #f4f4f4;
            margin-left: 0;
            &:last-child {
              border: 0;
              margin: 0;
              padding-bottom: 0;
            }
          }
        }
        .item-thumbnail {
          float: left;
          display: block;
          width: 80px;
          height: 80px;
          position: relative;
          z-index: 2;
          overflow: hidden;
          background-color: #cecece;
          &:before {
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background-color: rgba(0, 0, 0, 0);
            content: ' ';
            z-index: 3;
            pointer-events: none;
          }
          img {
            position: absolute;
            margin: auto;
            top: -9999px;
            right: -9999px;
            bottom: -9999px;
            left: -9999px;
            width: 150%;
            height: auto;
            z-index: 1;
          }
        }
        .item-title {
          line-height: 1.4;
          color: #777;
          font-size: 16px;
          font-weight: bold;
          font-family: Droid Serif;
          background: #f9f9f9;
          min-height: 80px;
          position: relative;
          padding: 15px;
          overflow: hidden;
          text-transform: uppercase;
          a {
            color: #777;
            text-decoration: none;
            font-family: Droid Serif;
          }
        }
      }
    }
  }
}
</style>
