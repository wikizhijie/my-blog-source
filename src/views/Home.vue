<template>
  <div class="home">
    <div class="container">
      <div class="section-heading">
        <h2>wiki的博客</h2>
        <div class="line-dec"></div>
        <span
          >想想做前端也三年了，一直想着弄一个自己的博客，也就是现在才抽出空来自己写了一个，也正好想用vue做这么一个博客，后期应该会加上用node做的后台，和管理后台，自己在这里写一些自己的想法跟对自己的知识归纳吧,
          额..... 好像还有点简历的感觉</span
        >
      </div>
      <div class="left-image-post">
        <div class="row">
          <div class="col-md-6">
            <div class="left-image">
              <img src="assets/images/func.jpeg" alt="" />
            </div>
          </div>
          <div class="col-md-6">
            <div class="right-text">
              <h4>JavaScript 函数式编程 初尝试</h4>
              <p>
                最近在看关于JavaScript函数式编程，恰巧也是因为react跟vue3.0推动，让更多前端开发的同学认知到函数式编程带来的一些优势，我也写一些最近自己一些刚刚开始学习函数式编程道路上的心得及感悟吧.....
              </p>
              <div class="white-button">
                <a href="#">Read More</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="right-image-post">
        <div class="row">
          <div class="col-md-6">
            <div class="left-text">
              <h4>关于页面权限的一些想法</h4>
              <p>
                在做一些管理后台的网站的时候，很多人都会有这样的需求，就是关于权限的问题....
              </p>
              <div class="white-button">
                <a href="#">Read More</a>
              </div>
            </div>
          </div>
          <div class="col-md-6">
            <div class="right-image">
              <img src="assets/images/right-image.jpg" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home"
};
</script>

<style lang="scss" scoped>
.home {
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
</style>
