<template>
  <section class="section3">
    <p class="title">
      건물이 기술 그 자체
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
        <!-- img :src에 require 넣지 않으면 이미지가 나타나지 않음 -->
        <img v-for="item in 121"
          :key="item"
          :src="require(`@/assets/images/section3/${item.toString()}.jpg`)"
        >
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

    titleTransform() {
      return `translate(-50%, -${this.scrollTop - 500}%)`
    },

    titleOpacity() {
      if (this.scrollTop < 550)
        return Math.min(60, this.scrollTop - 500) * 0.05
      return 1 - Math.min(60, this.scrollTop - 580) * 0.05
    },

    descOpacity() {
      return Math.min(30, this.scrollTop - 620) * 0.03
    },

    descTransform() {
      return `translate(-50%, -${this.scrollTop - 600}%)`
    },

    imgWidth() {
      return `${45 + Math.min(0, Math.max(50, (this.scrollTop - 200)))}%`
      // return `700px`
      // 원래 700px, 점점 100%
    },

    imgHeight() {
      // return (Math.min(0, Math.max(100, this.scrollTop - 600))) + '%'
      return `${Math.min(10, Math.max(500, this.scrollTop - 600))}%`
      // return `100px`
      // 원래 0, 점점 100
    },

    imgTransform() {
      return `translate(-50%, 100%)`
    }
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
  height: 900vh;
  margin-top: -200vh;
  background: #000;
  opacity: v-bind('bgOpacity');

  // opacity: .2;

  .title {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: v-bind('titleTransform');
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
    transform: v-bind('descTransform');
    color: #fff;
    font-size: 2.6em;
    line-height: 40px;
    text-align: center;
    opacity: v-bind('descOpacity');

    .desc1:nth-child(2) {
      margin-bottom: 30px;
    }
  }

  .video_wrap {
    position: fixed;
    top: 50%;
    left: 50%;
    width: v-bind('imgWidth');
    height: v-bind('imgHeight');
    transform: v-bind('imgTransform');
    background: white;


    .video {
      position: absolute;
      top: 0;
      left: 0;

      img {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
}
</style>