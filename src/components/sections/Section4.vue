<!-- 검정배경 Tech , New Normal, Eco, With,  -->

<template>
  <div class="section3">
    <div class="section3_bg">
      <div class="roll">
        TECH -> TECH -> TECH ->
      </div>
      <h2 class="title">TECH</h2>
      <p class="subtitle">로봇과 함께하는 일상</p>
      <p class="desc_1">로봇이 우리 삶에 자연스럽게 녹아드는 세상을 준비합니다.</p>
      <p class="desc_2">이를 앞당길 거대한 실험이 1784에서 시작되었습니다.</p>
      <p class="desc_3">네이버의 로보틱스, 자율주행, AI, 5G, 클라우드 기술과</p>
      <p class="desc_4">혁신적 인프라들이 하나로 융합됩니다.</p>
      <p class="desc_5">세계 최초 로봇 친화형 건물 - 스마트도시협회 인증 2022</p>
    </div>
  </div>
</template>

<script>
</script>

<style scoped lang="scss">
.section3 {
  position: relative;
  top: 3000px;
  width: 100%;
  height: 2000px;
  background: linear-gradient(145deg, #000, #fff);

  .section3_bg {
    position: sticky;
    top: 0;
    width: 100%;
    height: 100vh;

    .roll {
      position: absolute;
      background: #92a8d1;
      width: 60px;
      height: 100vh;
      color: #fff;
      font-size: 2em;
    }

    h2 {
      color: #fff;
      font-size: 6em;
      font-family: 'NanumSquareNeoHeavy';
      transform: translate(150px, 150px);
    }

    p {
      color: #fff;
    }

    .subtitle {
      font-size: 3em;
      transform: translate(150px, 200px);
    }

    .desc_1,
    .desc_2,
    .desc_3,
    .desc_4 {
      font-size: 1.3em;
      line-height: 20px;
      transform: translate(150px, 220px);
    }

    .desc_5 {
      font-size: 1.2em;
      color: #ccc;
      font-family: 'NanumSquareNeoLight';
      transform: translate(150px, 230px);
    }


  }
}
</style>