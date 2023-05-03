<!-- 혁신을 현실로 ~ 스크롤마다 프레임~~~~ -->

<template>
  <section class="section2">
    <div class="section2_bg">
      <picture>
        <source srcset="@/assets/images/section2.jpg">
        <img srcset="@/assets/images/section2.jpg" alt="네이버 건물">
      </picture>
    </div>
    <p class="section2_title">
      혁신을 현실로.
    </p>
  </section>
</template>

<script>
// window.addEventListener('scroll', function () {
//   console.log(window.scrollY)
// });
// 스크롤 위치 구하기

export default {
  name: 'Section2',

  computed: {
    titleFontSize() {
      return (10 + Math.min(100, Math.max(0, this.scrollTop - 200))) + 'em'
    },

    titleOpacity() {
      if (this.scrollTop < 150)
      return Math.min(20, this.scrollTop - 120) * 0.05
      return 1 - Math.min(40, this.scrollTop - 200) * 0.03
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
.section2 {
  position: relative;
  width: 100vw;
  height: 400vh;

  // background: pink;
  // height: 2000px;

  .section2_bg {
    // sticky? background-attachment?

    position: sticky;
    top: 0px;
    width: 100%;

    // background-attachment: fixed;
    // height: 3000px;
    // 이미지 뭐로 하지...

    picture {
      position: absolute;
      top: 0;
      left: 0;

      img {
        position: absolute;
        width: 100vw;
        height: 100vh;
        object-fit: cover;
      }

      // opacity: .2;
      // background-color: pink;
    }
  }

  .section2_title {
    position: fixed;
    top: 50%;
    left: 50%;
    color: #fff;
    font-size: v-bind('titleFontSize');
    font-family: 'NanumSquareNeoExtraBold';
    transform: translate(-50%, -50%);
    opacity: v-bind('titleOpacity');
    white-space: nowrap;
  }
}
</style>