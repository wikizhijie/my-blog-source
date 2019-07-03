<template>
  <div id="app">
    <div class="responsive-nav">
      <i class="fa fa-bars" id="menu-toggle"></i>
      <div id="menu" class="menu">
        <i class="fa fa-times" id="menu-close"></i>
        <div class="container">
          <div class="image">
            <a href="#"
              ><img src="./assets/images/author-image.jpeg" alt=""
            /></a>
          </div>
          <div class="author-content">
            <h4>wiki</h4>
            <span>Frontend devloper</span>
          </div>
          <nav class="main-nav" role="navigation">
            <ul class="main-menu">
              <li
                @click="handleTabClick('proface')"
                :class="{ active: active === 'proface' }"
              >
                <a>前言</a>
              </li>
              <li
                @click="handleTabClick('fp')"
                :class="{ active: active === 'fp' }"
              >
                <a>函数式编程</a>
              </li>
              <li
                @click="handleTabClick('vue')"
                :class="{ active: active === 'vue' }"
              >
                <a>Vue</a>
              </li>
              <li
                @click="handleTabClick('cm')"
                :class="{ active: active === 'cm' }"
              >
                <a>Contact Me</a>
              </li>
            </ul>
          </nav>
          <div class="social-network">
            <ul class="soial-icons">
              <li>
                <a href="https://fb.com/templatemo"
                  ><i class="fa fa-facebook"></i
                ></a>
              </li>
              <li>
                <a href="#"><i class="fa fa-twitter"></i></a>
              </li>
              <li>
                <a href="#"><i class="fa fa-linkedin"></i></a>
              </li>
              <li>
                <a href="#"><i class="fa fa-dribbble"></i></a>
              </li>
              <li>
                <a href="#"><i class="fa fa-rss"></i></a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <section class="section about-me" data-section="section1">
      <router-view />
    </section>
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      active: "proface"
    };
  },
  methods: {
    handleTabClick(tabtext) {
      this.active = tabtext;
    }
  }
};
</script>
<style lang="scss">
body {
  padding: 0;
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji",
    "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji", "Lato", sans-serif;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  color: #212529;
  text-align: left;
  background-color: #fff;

  li {
    list-style: none;
  }
  a {
    text-decoration: none;
  }
}
</style>
<style lang="scss" scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: url(./assets/images/page-bg.jpg) no-repeat center center fixed;
  background-size: cover;
  width: 100%;
  height: 100%;
  overflow-x: hidden;

  .menu {
    left: 10%;
    -webkit-transition: -webkit-transform 233ms cubic-bezier(0, 0, 0.21, 1);
    -webkit-overflow-scrolling: touch;
    background-color: #a43f49;
    box-sizing: border-box;
    height: 100vh;
    max-height: 100vh !important;
    max-width: 80vw !important;
    min-width: 45px !important;
    outline: none;
    overflow-x: hidden !important;
    overflow-y: auto !important;
    padding: 0;
    position: fixed !important;
    top: calc(90px);
    width: 20%;
    will-change: transform;
    z-index: 9999 !important;
    text-align: center;

    @media screen and (max-width: 1680px) {
      left: 5%;
    }

    .container {
      margin: 0 auto;

      .image {
        margin-top: 60px;

        a {
          text-decoration: none;

          img {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            text-align: center;
          }
        }
      }
    }
    .author-content {
      margin: 40px 0px 60px 0px;
      h4 {
        font-size: 26px;
        font-weight: 700;
        color: #fff;
        letter-spacing: 0.25px;
      }
      span {
        font-size: 13px;
        font-style: italic;
        color: #fff;
      }
    }
    .main-menu {
      padding: 0;
      margin: 0;
      list-style: none;

      li {
        &:hover {
          a {
            background: #fff;
            color: #8c363e;
          }
        }
        &.active {
          a {
            background: #fff;
            color: #8c363e;
          }
        }
        a {
          height: 70px;
          line-height: 70px;
          display: inline-block;
          font-size: 16px;
          font-weight: 700;
          color: #fff;
          width: 100%;
          transition: all 0.5s;
          border-top: 2px solid #fff;
          text-decoration: none;
        }
      }
    }
  }
  .section {
    color: #fff;
    width: 55%;
    right: 10%;
    left: 35%;
    position: relative;
    min-height: 100vh;
    padding-bottom: 80px;
    border-bottom: 3px solid rgba(250, 250, 250, 0.25);

    @media screen and (max-width: 1680px) {
      width: 65%;
      right: 5%;
      left: 30%;
    }
    .container {
      width: 100%;
      padding-right: 15px;
      padding-left: 15px;
      text-align: left;

      @media (min-width: 576px) {
        max-width: 540px;
      }
      @media (min-width: 768px) {
        max-width: 720px;
      }
      @media (min-width: 992px) {
        max-width: 960px;
      }
      @media (min-width: 1200px) {
        max-width: 1140px;
      }
      .section-heading {
        text-align: center;
        padding: 80px 45px;

        h2 {
          font-size: 32px;
          font-weight: 700;
          color: #fff;
        }
        .line-dec {
          width: 60px;
          height: 3px;
          background-color: #a43f49;
          margin: 10px auto;
        }
        span {
          margin-top: 5px;
          font-size: 16px;
          color: #fff;
          letter-spacing: 0.5px;
        }
      }
      .row {
        display: flex;
        flex-wrap: wrap;
        margin-right: -15px;
        margin-left: -15px;

        .col-md-6 {
          position: relative;
          width: 100%;
          padding-right: 15px;
          padding-left: 15px;

          @media (min-width: 768px) {
            flex: 0 0 50%;
            max-width: 50%;
          }
        }
      }
      .right-image-post {
        margin-top: 60px;
        padding-top: 60px;
        border-top: 2px solid rgba(250, 250, 250, 0.1);
      }
    }
  }
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
