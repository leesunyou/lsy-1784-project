<!-- 혁신을 현실로 ~ 스크롤마다 프레임~~~~ -->

<template>
  <section>
    <div class="section2">
      <div class="section2_bg">
        <p class="section2_title">
          혁신을 현실로.
        </p>
        <p class="section2_subtitle">
          건물이 기술 그 잡채~
        </p>
        <p class="desc_1">기술은 혼자 존재할 때 보다 서로 연결되고 합쳐질 때</p>
        <p class="desc_2">더 큰 의미를 갖습니다.</p>
        <p class="desc_3">공간-기술-사람-로봇이 촘촘히 연결되고 융합되는</p>
        <p class="desc_4">도전 속에 일상을 변화시킬 새로움을 만드는 것,</p>
        <p class="desc_5">이것이 우리가 테크 컨버전스에 집중하는 이유입니다.</p>
      </div>
    </div>
  </section>
</template>

<script>

window.addEventListener('scroll', function () {
  console.log(window.scrollY)
});

// $(window).scroll(function() {
//   var height = $(window).scrollTop();
//   $('.section2_title').eq(0).css('opacity', y);
// });
</script>

<style scoped lang="scss">
section {
  position: relative;
  top: 2200px;
  width: 100%;
  height: 3000px;
  background: linear-gradient(145deg, #000, #fff);

  .section2 {
    position: sticky;
    top: 0px;
    width: 100%;
    height: 100vh;
    background: url(@/assets/images/section2_3.jpg) no-repeat center/cover;
    // 이미지 뭐로 하지...

    .section2_bg {
      position: absolute;
      width: 100%;
      height: 700px;
    }

    .section2_title,
    .section2_subtitle,
    .desc_1,
    .desc_2,
    .desc_3,
    .desc_4,
    .desc_5 {
      color: #fff;
    }

    .section2_title {
      margin-top: 350px;
      font-size: 12em;
      text-align: center;
      font-family: 'NanumSquareNeoExtraBold';
    }

    .section2_subtitle {
      font-size: 12em;
      text-align: center;
      font-family: 'NanumSquareNeoExtraBold';
    }

    .desc_1,
    .desc_2,
    .desc_3,
    .desc_4,
    .desc_5 {
      font-size: 2.2em;
      text-align: center;
      line-height: 40px;
    }

    .desc_2 {
      margin-bottom: 30px;
    }
  }
}
</style>