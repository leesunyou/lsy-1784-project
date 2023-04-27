<!-- 들어오자마자 ~ 브랜드필름 보기 + 스토리 바로보기 -->
<!-- background에 영상 -->

<template>
  <div class="section1">
    <video muted autoplay loop>
      <source src="@/assets/video/section1.mp4" type="video/mp4">
    </video>
    <div class="bg_filter">
      <p class="title">1784</p>
      <p class="the">THE</p>
      <p class="test">TEST</p>
      <p class="bed">BED</p>
      <div class="arrow">
        <p>&#8659;</p>
      </div>

      <div class="naver_img">
        <img src="@/assets/images/naver.svg" alt="naver">
      </div>
      <p class="desc_1">1784는 네이버의 새로운 사옥이 가진 이름이자</p>
      <p class="desc_2">지번이며, 최초의 산업혁명이 시작된 해입니다.</p>
      <p class="desc_3">산업혁명이 인류의 삶을 바꿔 놓았던 것처럼,</p>
      <p class="desc_4">1784를 거대한 TESTBED 삼아 끊임없이</p>
      <p class="desc_5">실험하고 도전하며 새로운 내일을 만들어 갑니다.</p>

      <div class="brand_film">
        <a href="#">
          <p class="brand_title">브랜드 필름 보기</p>
          <p class="brand_arrow">&#8680;</p>
        </a>
      </div>

      <div class="story_now">
        <a href="#">
          <p class="story_title">스토리 바로 보기</p>
          <p class="story_arrow">&#8681;</p>
        </a>
      </div>
    </div>
  </div>
</template>

<script>

</script>

<style scoped lang="scss">
.section1 {
  // position: absolute;
  // top: 0;
  // height: 2200px;
  // width: 100%;

  video {
    position: fixed;
    // width: 100%;
    // height: 100vh;
    // height: 100%;
  }

  .bg_filter {
    position: absolute;
    top: 0;
    width: 100%;
    height: 400%;
    background: rgba(70, 70, 70, 0.3);
    // height: 2200px;
    // background-color: pink;

    .title {
      color: #fff;
      font-size: 68em;
      font-family: 'NanumSquareNeoExtraBold';
      // position: absolute;
      // top: 0;
      // background-color: pink;
    }

    .the,
    .test,
    .bed {
      color: #fff;
      font-size: 18em;
      font-family: 'NanumSquareNeoExtrabold';
    }

    .arrow {
      position: fixed;
      left: 50%;
      bottom: 30px;
      // position: absolute;
      // background-color: pink;

      p {
        color: #fff;
        font-size: 4em;
      }
    }

    .naver_img {
      width: 360px;
      margin: 0 auto;

      .naver {
        width: 100%;
      }
    }

    .desc_1,
    .desc_2,
    .desc_3,
    .desc_4,
    .desc_5 {
      color: #fff;
      font-size: 2.6em;
      text-align: center;
      line-height: 40px;
    }

    .desc_2 {
      margin-bottom: 30px;
    }

    .brand_film {
      width: 520px;
      height: 76px;
      margin: 0 auto;
      margin-top: 60px;
      border: 4px solid #fff;
      border-radius: 38px;
      transition: .5s;
      // background: pink;

      &:hover {
        background: rgba(0, 0, 0, .6);
      }

      a {
        display: block;
        position: relative;
        width: 100%;
        height: 62px;
        border-radius: 30px;
        // margin-bottom: 0px;
        // background: pink;

        p {
          display: inline-block;
          color: #fff;
          font-size: 2.2em;
        }

        .brand_title {
          margin-top: 24px;
          margin-left: 35px;
        }

        .brand_arrow {
          margin-left: 270px;
          // transform: translateY(0px);
          // background-color: pink;
        }
      }
    }

    .story_now {
      width: 520px;
      height: 76px;
      margin: 0 auto;
      margin-top: 30px;
      border: 1px solid #fff;
      border-radius: 38px;
      background: #fff;
      transition: .4s;

      &:hover {
        background: #000;
      }

      &:hover p {
        color: #fff;
      }

      a {
        display: block;
        position: relative;
        width: 100%;
        height: 62px;
        border-radius: 30px;
        // margin-bottom: ;

        p {
          display: inline-block;
          color: #000;
          font-size: 2.2em;
          transition: .4s;
        }

        .story_title {
          margin-top: 26px;
          margin-left: 35px;
        }

        .story_arrow {
          margin-left: 270px;
          transform: translateY(3px);
        }
      }
    }
  }
}
</style>