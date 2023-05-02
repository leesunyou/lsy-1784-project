<!-- 혁신을 현실로 ~ 스크롤마다 프레임~~~~ -->

<template>
  <section class="section2">
    <div class="section2_bg">
      <picture>
        <source srcset="@/assets/images/section2_3.jpg">
        <img srcset="@/assets/images/section2_3.jpg" alt="네이버 건물">
      </picture>
    </div>
    <p class="section2_title">
      혁신을 현실로.
    </p>
  </section>
</template>

<script>
window.addEventListener('scroll', function () {
  console.log(window.scrollY)
});
// 스크롤 위치 구하기

export default {
  name: 'Section2',

  computed: {
    titleFontSize() {
      return (9 + Math.min(100, Math.max(0, this.scrollTop - 200))) + 'em'
    },

    titleOpacity() {
      if (this.scrollTop < 300)
        return Math.min(300, this.scrollTop - 30) * 0.01
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
  height: 500vh;
  // background: pink;
  // height: 2000px;

  .section2_bg {
    // sticky? background-attachment?

    position: sticky;
    top: 0px;
    width: 100%;
    height: 100vh;

    // background-attachment: fixed;
    // height: 3000px;
    // 이미지 뭐로 하지...

    picture {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;

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
    color: #fff;
    left: 50%;
    transform: translate(-50%, -50%);
    font-family: 'NanumSquareNeoExtraBold';
    font-size: v-bind('titleFontSize');
    opacity: v-bind('titleOpacity');
    white-space: nowrap;
  }
}
</style>