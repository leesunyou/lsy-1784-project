<template>
  <section class="section5">
    <div class="main">
      <p class="title">
        우리의 도전은
        <br>
        진행형
      </p>

      <p class="sub">
        수많은 시행착오 속에서 던져진 도전과 질문은 새로운 정답을 찾아가는
        <br>
        과정이라 믿습니다.
        <br>
        오늘도 우리는 그 과정 속에서 성장하고 있고,
        <br>
        새로운 미래를 향한 실험과 도전은 계속되고 있습니다.
      </p>
    </div>

    <div class="container">
      <a href="#">
        <div class="box box1">
          <img src="@/assets/images/section5/img1.jpeg" alt="듣다보면 똑똑해지는 라이프">
          <div class="text_box">
            <p class="name">듣다보면 똑똑해지는 라이프</p>
            <p class="desc">SF 영화 속 미래기술</p>
          </div>
        </div>
      </a>

      <a href="#">
        <div class="box box2">
          <img src="@/assets/images/section5/img2.jpeg" alt="조승연의 탐구생활">
          <div class="text_box">
            <p class="name">조승연의 탐구생활</p>
            <p class="desc">창의적인 공간의 조건</p>
          </div>
        </div>
      </a>

      <a href="#">
        <div class="box box3">
          <img src="@/assets/images/section5/img3.jpeg" alt="김지윤의 지식 PLAY">
          <div class="text_box">
            <p class="name">김지윤의 지식 PLAY</p>
            <p class="desc">로봇 석학이 말하는 1784</p>
          </div>
        </div>
      </a>

      <a href="#">
        <div class="box box4">
          <img src="@/assets/images/section5/img4.png" alt="1784 STORY">
          <div class="text_box">
            <p class="name">1784 STORY</p>
            <p class="desc">FaceSign의 독보적 기술력</p>
          </div>
        </div>
      </a>

      <a href="#">
        <div class="box box5">
          <img src="@/assets/images/section5/img5.jpeg" alt="1784 STORY">
          <div class="text_box">
            <p class="name">1784 STORY</p>
            <p class="desc">1784에 5G를 설치한 이유</p>
          </div>
        </div>
      </a>

      <a href="#">
        <div class="box box6">
          <img src="@/assets/images/section5/img6.jpeg" alt="네이버 디자인 콜로키움">
          <div class="text_box">
            <p class="name">네이버 디자인 콜로키움 '22</p>
            <p class="desc">인간과 기술이 공존하는 일터</p>
          </div>
        </div>
      </a>

    </div>

    <div class="contact">
      <p class="con_title">CONTACT</p>
      <div class="add_container">
        <div class="add_box">
          <div class="naver1784">
            <p class="naver1784_name">네이버 1784</p>
            <p class="naver1784_add">경기도 성남시 분당구 정자일로 95</p>
          </div>
          <div class="green">
            <p class="green_name">네이버 그린팩토리</p>
            <p class="green_add">경기도 성남시 분당구 불정로 6</p>
          </div>
        </div>
      </div>
      <div class="background"></div>
    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
.section5 {
  position: relative;
  width: 100%;
  height: 2000px;
  background: #fff;
  margin-top: 348.7vh;

  .main {
    position: relative;
    margin-bottom: 60px;

    .title {
      padding: 12% 5% 0px 15%;
      // padding: 200px 100px 0px 200px;
      font-size: 6em;
      line-height: 70px;
      // background-color: yellow;
      display: inline-block;
      font-family: 'NanumSquareNeoExtraBold';
    }

    .sub {
      font-family: 'NanumSquareNeoExtraBold';
      display: inline-block;
      line-height: 34px;
      font-size: 2.6em;
      // background-color: green;
      position: absolute;
      bottom: 0;
    }
  }

  .container {
    // background-color: green;
    max-width: 70%;
    margin: 0 auto;

    a {

      .box1,
      .box2,
      .box4,
      .box5 {
        margin-right: 30px;
      }

      .box1,
      .box2,
      .box3 {
        margin-bottom: 30px;
      }

      .box {
        width: calc((100% - 60px) / 3);
        background-color: yellow;
        display: inline-block;
        border-radius: 18px;
        overflow: hidden;
        box-shadow: 0 5px 20px 0 rgba(0, 0, 0, 0.1);

        img {
          width: 100%;
        }

        .text_box {
          background: #fff;
          height: 120px;

          .name {
            font-size: 2.1em;
            font-family: 'NanumSquareNeoExtraBold';
            text-align: center;
            padding-top: 30px;
          }

          .desc {
            font-size: 1.8em;
            text-align: center;
            margin-top: 10px;
            // background-color: pink;
          }
        }
      }
    }
  }

  .contact {
    margin-top: 200px;
    // background: pink;

    .con_title {
      font-size: 10em;
      font-family: 'NanumSquareNeoExtraBold';
      padding: 100px 100px 0px 100px;
      display: inline-block;
      // background-color: green;
    }

    .add_container {
      position: relative;
      margin-bottom: 50px;

      .add_box {
        // background-color: yellow;
        position: absolute;
        right: 100px;
        bottom: 20px;
        display: inline-block;

        .naver1784 {
          // background-color: salmon;
          margin-bottom: 20px;
          display: flex;

          .naver1784_name {
            margin-right: 50px;
            font-size: 2em;
            font-family: 'NanumSquareNeoExtraBold';
          }

          .naver1784_add {
            font-size: 2em;
            font-family: 'NanumSquareNeo';
          }
        }

        .green {
          display: flex;
          // background-color: slateblue;

          .green_name {
            font-size: 2em;
            margin-right: 50px;
            font-family: 'NanumSquareNeoExtraBold';
          }

          .green_add {
            font-size: 2em;
            font-family: 'NanumSquareNeo';
          }
        }

      }
    }

    .background {
      width: 100%;
      height: 700px;
      background: url(@/assets/images/section5/img7.jpeg) no-repeat center/cover;
    }
  }
}
</style>