<template>
  <section class="section3">
    <p class="title">
      건물이 기술 그 잡채~
    </p>
    <div class="desc">
      <p class="desc1">기술은 혼자 존재할 때 보다 서로 연결되고 합쳐질 때</p>
      <p class="desc1">더 큰 의미를 갖습니다.</p>

      <p class="desc2">공간-기술-사람-로봇이 촘촘히 연결되고 융합되는</p>
      <p class="desc2">도전 속에 일상을 변화시킬 새로움을 만드는 것,</p>
      <p class="desc2">이것이 우리가 테크 컨버전스에 집중하는 이유입니다.</p>
    </div>
    <div class="video_wrap">
      <div class="video">
        <img src="" alt="">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Section3',
  computed: {

    bgOpacity() {
      return Math.min(60, this.scrollTop - 450) * 0.02
    },

    titleOpacity() {
      if (this.scrollTop < 550)
        return Math.min(60, this.scrollTop - 500) * 0.05
      return 1 - Math.min(60, this.scrollTop - 580) * 0.05
    },

    titleTransform() {

    },

    descOpacity() {
      return Math.min(30, this.scrollTop - 620) * 0.03
    },

    descTransform() {

    },
  },

  props: ['scrollTop'],

  data() {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
.section3 {
  position: relative;
  width: 100vw;
  height: 600vh;
  margin-top: -200vh;
  background: #000;
  opacity: v-bind('bgOpacity');

  // opacity: .2;

  .title {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: #fff;
    font-size: 9em;
    font-family: 'NanumSquareNeoExtraBold';
    opacity: v-bind('titleOpacity');
    white-space: nowrap;
  }

  .desc {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: #fff;
    font-size: 2.6em;
    line-height: 40px;
    text-align: center;
    opacity: v-bind('descOpacity');
    // transition: .5s;

    .desc1:nth-child(2) {
      margin-bottom: 30px;
    }
  }
}
</style>