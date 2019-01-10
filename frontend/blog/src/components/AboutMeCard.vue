<template>
  <div style="perspective: 800px;">
    <transition mode="out-in" :enter-class="enterClass" :leave-to-class="leaveToClass">
      <b-card
        no-body
        :img-src="banner"
        v-if="flipping"
        img-alt="Jason"
        img-top
        tag="article"
        align="center"
        class="mb-2"
        key="1"
        style="transform-style: preserve-3d;"
      >
        <p class="card-avatar">
          <img :src="avatar" alt="Jason">
        </p>
        <b-card-body>
          <p class="card-title">Mr. Jason Lee</p>
          <p class="card-text">Web Developer</p>
          <p class="card-click" @click="flip()">
            <font-awesome-icon icon="sync-alt"/>Click here to learn more about me
          </p>
        </b-card-body>
      </b-card>
      <b-card
        overlay
        :img-src="bannerBig"
        v-else
        img-alt="Jason"
        img-fluid
        tag="article"
        align="center"
        class="mb-2"
        key="2"
        style="transform-style: preserve-3d;"
      >
        <div class="over"></div>
        <b-card-body class="card2">
          <div class="card-text">
            <h2>About me</h2>
            <hr>
            <p
              class="paragraph"
            >More than 8 years experience of web development, more than 5 years experience of web development teaching and training. Talented Senior Software Engineer proficient in all phases of the software development lifecycle. Adept at working with Agile and Scrum methodologies to accomplish project milestones according to specific timeframes. Able to use AWS, PHP, HTML, CSS, JavaScript, VueJS, MySQL and Linux and other programming languages to complete work. Highly organized and detail-oriented professional with 8 years of progressive experience in the field.</p>
            <hr>
            <p>
              <a href="https://www.facebook.com/profile.php?id=100001472784145" target="_blank">
                <font-awesome-icon class="faicon facebook" :icon="['fab', 'facebook-square']"/>
              </a>
              <a href="https://www.linkedin.com/in/jason-lee-4a1003146/" target="_blank">
                <font-awesome-icon class="faicon linkedin" :icon="['fab', 'linkedin']"/>
              </a>
              <font-awesome-icon
                v-b-tooltip.click
                title="86267659"
                class="faicon wechat"
                :icon="['fab', 'weixin']"
              />
              <a href="mailto:mrjasonedu@gmail.com" title="mrjasonedu@gmail.com">
                <font-awesome-icon class="faicon email" :icon="['fas', 'at']"/>
              </a>
              <a href="https://github.com/BestJason" target="_blank">
                <font-awesome-icon class="faicon github" :icon="['fab', 'github']"/>
              </a>
            </p>
          </div>
          <p class="card-click" @click="flip()">
            <font-awesome-icon icon="sync-alt"/>Click here to learn more about me
          </p>
        </b-card-body>
      </b-card>
    </transition>
  </div>
</template>

<script>
import banner from '@/assets/imgs/banner.jpeg'
import bannerBig from '@/assets/imgs/banner_big.jpg'
import avatar from '@/assets/imgs/avatar.jpeg'

export default {
  name: 'AboutMeCard',
  data: () => {
    return {
      banner,
      bannerBig,
      avatar,
      flipping: false,
      enterClass: 'v-enter',
      leaveToClass: 'v-leave-to'
    }
  },
  methods: {
    flip () {
      this.flipping = !this.flipping
      this.enterClass = this.flipping ? 'v-enter' : 'v-enter-reverse'
      this.leaveToClass = this.flipping ? 'v-leave-to' : 'v-leave-to-reverse'
    }
  }
}
</script>

<style lang="scss" scoped>
html,
body {
  font-family: Roboto, sans-serif;
  .card {
    margin: 20px auto;
    width: 80%;
    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16),
      0 2px 10px 0 rgba(0, 0, 0, 0.12);
    border: 0;
    .card-img-top {
      max-height: 300px;
    }
    .img-fluid {
      height: 350px;
      max-height: 350px;
      border-radius: calc(0.25rem - 1px);
      box-shadow: 0 6px 15px 0 rgba(0, 0, 0, 0.46),
        0 2px 10px 0 rgba(0, 0, 0, 0.52);
    }
    .over {
      width: 100%;
      height: 100%;
      position: absolute;
      margin: -1.25rem;
      background-color: #000;
      border-radius: calc(0.25rem - 1px);
      opacity: 0.6;
      z-index: 1;
    }
    .card-body {
      font-weight: 700;
      .card-title {
        font-size: 30px;
      }
      .card-text {
        font-size: 15px;
        color: #2196f3;
      }
      .card-click {
        font-weight: 400;
        margin-bottom: 0px;
        color: gray;
        font-size: 15px;
        cursor: pointer;
        svg {
          margin-right: 3px;
          transition: all 0.8s ease;
          &:hover {
            transform: rotateZ(360deg);
          }
        }
      }
      &.card2 {
        z-index: 2;
        position: relative;
        .card-text {
          color: #fff;
          h2 {
            font-size: 30px;
          }
          hr {
            border-color: #bdbdbd;
          }
          .paragraph {
            font-weight: 400;
            min-height: 100px;
          }
          .faicon {
            font-size: 25px;
            margin: 0 15px;
            &.facebook {
              color: #00d6ff;
            }
            &.linkedin {
              color: #fff100;
            }
            &.wechat {
              color: #44ed06;
              cursor: pointer;
            }
            &.email {
              color: #51dee1;
            }
            &.github {
              color: #fff;
            }
          }
        }
        .card-click {
          color: #fff;
        }
      }
    }
    .card-avatar {
      background-color: #ffffff;
      margin-bottom: 0;
      img {
        border: 5px solid #fff;
        background: none repeat scroll 0 0 #fff;
        border-radius: 50%;
        margin-top: -60px;
        width: 120px;
        transition: all 0.8s ease;
        &:hover {
          transform: rotateZ(360deg);
        }
      }
    }
  }
  .v-enter-active,
  .v-leave-active {
    transform-style: preserve-3d;
    transition: all 0.3s linear;
  }
  .v-enter {
    transform: rotateY(-90deg);
  }
  .v-leave-to {
    transform: rotateY(90deg);
  }
  .v-enter-reverse {
    transform: rotateY(90deg);
  }
  .v-leave-to-reverse {
    transform: rotateY(-90deg);
  }
}
</style>
