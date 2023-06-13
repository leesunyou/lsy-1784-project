<template>
  <section class="section4">
    <div class="section4_bg">
      <div class="roll">
        <div v-for="item in item" class="textbox">
          <p class="text">{{ text }}</p>
          <p class="arrow">{{ arrow }}</p>
        </div>
      </div>

      <div class="tech">
        <h2 class="main_title">TECH</h2>

        <div class="tech_cont">
          <div class="tech_main">
            <p class="sub_title">로봇과 함께하는 일상</p>
            <p class="desc_1">
              로봇이 우리 삶에 자연스럽게 녹아드는 세상을 준비합니다.
              <br>
              이를 앞당길 거대한 실험이 1784에서 시작되었습니다.
              <br>
              네이버의 로보틱스, 자율주행, AI, 5G, 클라우드 기술과
              <br>
              혁신적 인프라들이 하나로 융합됩니다.
            </p>
            <p class="desc_2">
              세계 최초 로봇 친화형 건물 - 스마트도시협회 인증 2022
            </p>
            <div class="tech_main_img">
              <img src="@/assets/images/section4/tech_main_1.jpeg" alt="naver1784">
            </div>
          </div>

          <div class="tech_box" v-for="t_box1 in tech_box1" :key="t_box1">
            <img :src="t_box1.img" alt="tech이미지">
            <div class="text_box">
              <p class="box_name">{{ t_box1.name }}</p>
              <p class="box_desc" v-html="t_box1.desc"></p>
            </div>
          </div>
        </div>

        <div class="tech_cont">
          <p class="sub_title">일하는 모습의 미래</p>
          <p class="desc_1">
            1784에서는 생활하고 일하는 방식이 새롭게 설계됩니다.
            <br>
            건물 곳곳에 스며든 네이버의 다양한 선행 기술이 더 나은
            <br>
            업무 환경을 만들고 그 안에서 일하는 모습은
            <br>
            미래의 새로운 기준이 됩니다.
          </p>
          <div class="tech_main_img">
            <img src="@/assets/images/section4/tech_main_2.jpeg" alt="naver1784">
          </div>

          <div class="tech_box" v-for="t_box2 in tech_box2" :key="t_box2">
            <img :src="t_box2.img" alt="tech이미지">
            <div class="text_box">
              <p class="box_name">{{ t_box2.name }}</p>
              <p class="box_desc" v-html="t_box2.desc"></p>
            </div>
          </div>
        </div>

      </div>

      <div class="new_normal">
        <h2 class="main_title">NEW NORMAL</h2>

        <div class="new_cont">
          <p class="sub_title">설계부터 다르게</p>
          <p class="desc_1">
            지속 가능하며 표준화된 시스템으로, 팬데믹 이후에도
            <br>
            모두가 안전하게 일할 수 있는 공간을 만들어 갑니다.
          </p>
          <div class="new_main_img">
            <img src="@/assets/images/section4/new_main_1.jpeg" alt="naver1784">
          </div>

          <div class="new_box" v-for="n_box1 in new_box1" :key="n_box1">
            <img :src="n_box1.img" alt="new이미지">
            <div class="text_box">
              <p class="box_name">{{ n_box1.name }}</p>
              <p class="box_desc" v-html="n_box1.desc"></p>
            </div>
          </div>
        </div>
      </div>

      <div class="eco">
        <h2 class="main_title">ECO</h2>

        <div class="eco_cont">
          <p class="sub_title">건물 자체가 친환경 시스템</p>
          <p class="desc_1">
            자연 에너지를 이용하는 것에 그치지 않고,
            <br>
            에너지 절감까지 가능한 친환경 인프라 시스템을 만들었습니다.
          </p>
          <div class="eco_main_img">
            <img src="@/assets/images/section4/eco_main_1.jpeg" alt="naver1784">
          </div>

          <div class="eco_box" v-for="e_box1 in eco_box1" :key="e_box1">
            <img :src="e_box1.img" alt="eco이미지">
            <div class="text_box">
              <p class="box_name">{{ e_box1.name }}</p>
              <p class="box_desc" v-html="e_box1.desc"></p>
            </div>
          </div>
        </div>
      </div>

      <div class="with">
        <h2 class="main_title">ECO</h2>

        <div class="with_cont">
          <p class="sub_title">건물 자체가 친환경 시스템</p>
          <p class="desc_1">
            자연 에너지를 이용하는 것에 그치지 않고,
            <br>
            에너지 절감까지 가능한 친환경 인프라 시스템을 만들었습니다.
          </p>
          <div class="with_main_img">
            <img src="@/assets/images/section4/with_main_1.jpeg" alt="naver1784">
          </div>

          <div class="with_box" v-for="w_box1 in with_box1" :key="w_box1">
            <img :src="w_box1.img" alt="with_이미지">
            <div class="text_box">
              <p class="box_name">{{ w_box1.name }}</p>
              <p class="box_desc" v-html="w_box1.desc"></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      tech_box1: [
        {
          img: require("@/assets/images/section4/tech_1_1.jpeg"),
          name: '서비스 로봇 Rookie',
          desc: '5G 브레인리스 로봇 기술을 기반으로<br>1784에서 다양한 서비스를 제공하는 로봇'
        },
        {
          img: require("@/assets/images/section4/tech_1_2.jpeg"),
          name: 'ROBOPORT',
          desc: '로봇들의 자유로운 층간 이동을 돕는<br>세계 최초의 로봇 전용 엘리베이터'
        },
        {
          img: require("@/assets/images/section4/tech_1_3.jpeg"),
          name: 'ARC',
          desc: '네이버 클라우드와 5G 네트워크 기반의<br>멀티 로봇 인텔리전스 시스템'
        }
      ],

      tech_box2: [
        {
          img: require("@/assets/images/section4/tech_2_1.jpeg"),
          name: 'CLOVA FaceSign',
          desc: '마스크를 써도, 멈추지 않고 이동하면서도 자연스럽게<br>누군지 식별 가능한 얼굴 인식 디바이스'
        },
        {
          img: require("@/assets/images/section4/tech_2_2.jpeg"),
          name: 'WORKS 비서',
          desc: '로봇 딜리버리, 식음료 주문, 주차위치 확인까지,<br>각종 생활 지원 서비스들을 앱 하나로 해결'
        },
        {
          img: require("@/assets/images/section4/tech_2_3.jpeg"),
          name: '스마트제어',
          desc: '조명, 온도, 환기 등 건물 어디서나<br>모바일로 업무 환경을 바로 제어'
        },
        {
          img: require("@/assets/images/section4/tech_2_4.jpeg"),
          name: 'NAVER CARE',
          desc: 'AI를 활용한 신체 계측, 비대면 스마트 문진 등<br>네이버 기술을 담은 미래 헬스케어 연구'
        }
      ],

      new_box1: [
        {
          img: require("@/assets/images/section4/new_1.jpeg"),
          name: '독립 공조 환기 시스템',
          desc: '감염 예방을 위해 각 층별로<br>분리된 환기 시스템을 적용'
        },
        {
          img: require("@/assets/images/section4/new_2.jpeg"),
          name: '방역 자문단',
          desc: '설계부터 감염 내과 전문의,<br>산업공학 전문가와 컨설팅 진행'
        },
        {
          img: require("@/assets/images/section4/new_3.jpeg"),
          name: 'NAVER 부속의원',
          desc: '세분화된 전문의 진료와 건강 상담까지<br>네이버의 기술이 더해진 의료 서비스 제공'
        },
        {
          img: require("@/assets/images/section4/new_4.jpeg"),
          name: '언택트 워크플레이스 리포트',
          desc: '팬데믹 시대 새로운 오피스에 대한 고민'
        }
      ],

      eco_box1: [
        {
          img: require("@/assets/images/section4/eco_1.jpeg"),
          name: '더블스킨',
          desc: '이중 창호와 바람길을 내어<br>햇빛으로 인한 열을 자연적으로 배출'
        },
        {
          img: require("@/assets/images/section4/eco_2.jpeg"),
          name: '복사 냉방 시스템',
          desc: '천장에 흐르는 차가운 물로<br>쾌적한 실내 온도 유지'
        },
        {
          img: require("@/assets/images/section4/eco_3.jpeg"),
          name: 'LED 조명 & 제어 시스템',
          desc: '친환경 LED 조명을 모바일로 손쉽게 제어'
        }
      ],

      with_box1: [
        {
          img: require("@/assets/images/section4/with_1.jpeg"),
          name: 'D2SF@분당',
          desc: '기술 스타트업과 교류하고 협력하며<br>더 큰 성장의 기회를 만드는 스타트업 입주 공간'
        },
        {
          img: require("@/assets/images/section4/with_2.jpeg"),
          name: 'KAIST-NAVER AI Center',
          desc: '기술과 인프라를 공유하고 AI 전문 인재들을 키워내는 초창의적 AI 공동연구센터'
        },
        {
          img: require("@/assets/images/section4/with_3.jpeg"),
          name: '모바일테스트룸',
          desc: '200여 대의 다양한 디바이스로<br>서비스 테스트가 가능한 공간'
        }
      ]
    }
  }
}

</script>

<style scoped lang="scss">
.section4 {
  position: relative;
  top: 3000px;
  width: 100%;
  height: 2000vh;
  background: pink;

  .section4_bg {
    position: sticky;
    top: 0px;
    width: 100%;
    // height: 200vh;

    .main_title,
    .sub_title,
    .desc_1 {
      color: #fff;
      // color - if scrollTop 해서 #000으로 색상 변경
    }

    .main_title {
      padding-top: 180px;
      margin-left: 85px;
      margin-bottom: 40px;
      // background-color: pink;
      font-size: 6.5em;
      font-family: 'NanumSquareNeoHeavy';
    }

    .sub_title {
      margin-bottom: 15px;
      font-size: 3em;
      font-family: 'NanumSquareNeoExtraBold';
    }

    .desc_1 {
      font-size: 1.3em;
      line-height: 20px;
      margin-bottom: 10px;
    }

    .desc_2 {
      font-size: 1.3em;
      color: #ccc;
      margin-bottom: 30px;
    }

    .text_box {
      width: 320px;
      height: 150px;
      position: absolute;
      bottom: 0;
      background: rgba(0, 0, 0, .1);
      backdrop-filter: saturate(180%) blur(20px);

      .box_name,
      .box_desc {
        color: #fff;
        // 항상 #fff
      }
    }

    .box_name {
      font-size: 1.6em;
      text-align: center;
    }

    .box_desc {
      font-size: 1.2em;
      text-align: center;
    }

    .roll {

      .textbox {

        .text {}

        .arrow {}
      }
    }

    .tech {
      // background: #000;

      .tech_cont {

        .tech_main {
          width: 320px;
          margin-right: 170px;
          display: inline-block;
          // background-color: pink;
          margin-left: 85px;

          .tech_main_img {

            img {
              width: 320px;
            }
          }
        }

        .tech_box {
          position: relative;
          background: gray;
          width: 320px;
          height: 450px;
          display: inline-block;
          border-radius: 20px;
          overflow: hidden;
          margin-right: 30px;

          img {
            width: 100%;
          }
        }
      }
    }
  }




}
</style>