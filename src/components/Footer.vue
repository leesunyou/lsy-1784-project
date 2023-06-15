<template>
  <footer class="footer">
    <a href="#" class="naver_logo">
      <div class="logo_wrap">
        <img src="@/assets/images/footer/logo.png" alt="naver">
      </div>
    </a>

    <p class="sub">1784</p>

    <ul class="site">
      <li><a href="#">NAVER CLOUD</a></li>
      <li><a href="#">WORKS MOBILE</a></li>
      <li><a href="#">SNOW</a></li>
      <li><a href="#">NAVER LABS</a></li>
      <li><a href="#">NAVER WEBTOON</a></li>
      <li class="last_li"><a href="#">NAVER FINANCIAL</a></li>
    </ul>

    <p class="copy">
      Copyright @ NAVER corp. All rights reserved.
    </p>
  </footer>
</template>

<script>

</script>

<style scoped lang="scss">
footer {
  position: relative;
  background: #000;
  width: 100%;
  margin-top: 255px;
  height: 180px;

  .naver_logo {

    .logo_wrap {
      position: absolute;
      // background-color: pink;
      width: 120px;
      margin-left: 100px;
      top: 30px;

      img {
        width: 100%;
      }
    }
  }

  .sub {
    color: #fff;
    font-size: 2.5em;
    position: absolute;
    top: 30px;
    right: 100px;
  }

  .site {
    display: flex;
    // background-color: pink;
    position: absolute;
    top: 90px;
    left: 100px;

    li {

      &::after {
        margin-left: 15px;
        margin-right: 15px;
        content: '|';
        color: #777;
      }

      a {
        font-size: 1.4em;
        color: #fff;
      }
    }

    .last_li {

      &::after {
        content: none;
      }
    }


  }

  .copy {
    color: #fff;
    position: absolute;
    bottom: 30px;
    font-size: 1.4em;
    color: #aaa;
    left: 100px;
  }
}
</style>