<template>
  <div class="port__cont container">
    <div v-for="(text, index) in portText" :key="index" class="port">
      <figure class="port__header">
        <router-link :to="text.url">
          <img :src="text.portImg" :alt="text.title" />
        </router-link>
      </figure>
      <div class="port__body">
        <div>
          <img :src="text.iconImg" :alt="text.desc" />
        </div>
        <div>
          <h4>{{ text.title }}</h4>
          <p>{{ text.desc }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      portText: [
        {
          portImg: "../assets/images/port/베르나르 베르베르01.png",
          iconImg: "../assets/images/member/peep-27-1.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=146610828",
          title: "고양이",
          desc: "베르나르 베르베르",
        },
        {
          portImg: "../assets/images/port/베르나르 베르베르02.png",
          iconImg: "../assets/images/member/peep-27-1.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=2253337",
          title: "파피용",
          desc: "베르나르 베르베르",
        },
        {
          portImg: "../assets/images/port/베르나르 베르베르03.png",
          iconImg: "../assets/images/member/peep-27-1.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=32136853",
          title: "제3인류",
          desc: "베르나르 베르베르",
        },
        {
          portImg: "../assets/images/port/베르나르 베르베르04.png",
          iconImg: "../assets/images/member/peep-27-1.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=294835271",
          title: "행성",
          desc: "베르나르 베르베르",
        },
        {
          portImg: "../assets/images/port/베르나르 베르베르05.png",
          iconImg: "../assets/images/member/peep-27-1.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=364908",
          title: "뇌",
          desc: "베르나르 베르베르",
        },
        {
          portImg: "../assets/images/port/베르나르 베르베르06.png",
          iconImg: "../assets/images/member/peep-27-1.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=293057",
          title: "아버지들의 아버지",
          desc: "베르나르 베르베르",
        },
        {
          portImg: "../assets/images/port/기욤뮈소01.png",
          iconImg: "../assets/images/member/peep-54.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=286922889",
          title: "당신거기 있어줄래요?",
          desc: "기욤 뮈소",
        },
        {
          portImg: "../assets/images/port/기욤뮈소02.png",
          iconImg: "../assets/images/member/peep-54.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=286920811",
          title: "구해줘",
          desc: "기욤 뮈소",
        },
        {
          portImg: "../assets/images/port/기욤뮈소03.png",
          iconImg: "../assets/images/member/peep-54.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=286765514",
          title: "센 강의 이름모를 여인",
          desc: "기욤 뮈소",
        },
        {
          portImg: "../assets/images/port/기욤뮈소04.png",
          iconImg: "../assets/images/member/peep-54.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=317302949",
          title: "종이 여자",
          desc: "기욤 뮈소",
        },
        {
          portImg: "../assets/images/port/기욤뮈소05.png",
          iconImg: "../assets/images/member/peep-54.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=306367260",
          title: "안젤리크",
          desc: "기욤 뮈소",
        },
        {
          portImg: "../assets/images/port/기욤뮈소06.png",
          iconImg: "../assets/images/member/peep-54.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=216722228",
          title: "작가들의 비밀스러운 삶",
          desc: "기욤 뮈소",
        },
        {
          portImg: "../assets/images/port/jk롤링01.png",
          iconImg: "../assets/images/member/peep-101.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=226215686",
          title: "혼혈왕자",
          desc: "jk롤링",
        },
        {
          portImg: "../assets/images/port/jk롤링02.png",
          iconImg: "../assets/images/member/peep-101.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=215741930",
          title: "불의 잔",
          desc: "jk롤링",
        },
        {
          portImg: "../assets/images/port/jk롤링03.png",
          iconImg: "../assets/images/member/peep-101.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=215741756",
          title: "비밀의 방",
          desc: "jk롤링",
        },
        {
          portImg: "../assets/images/port/jk롤링04.png",
          iconImg: "../assets/images/member/peep-101.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=221588157",
          title: "불사조 기사단",
          desc: "jk롤링",
        },
        {
          portImg: "../assets/images/port/jk롤링05.png",
          iconImg: "../assets/images/member/peep-101.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=215739377",
          title: "마법사의 돌",
          desc: "jk롤링",
        },
        {
          portImg: "../assets/images/port/jk롤링06.png",
          iconImg: "../assets/images/member/peep-101.svg",
          url: "https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=120343185",
          title: "저주받은 아이",
          desc: "jk롤링",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.port__cont {
  @include flex-between;
  margin-bottom: 120px;

  flex-wrap: wrap;
  .port {
    width: 32%;
    margin-bottom: 20px;
    .port__header {
      margin-bottom: 20px;
      img {
        width: 100%;
      }
    }
    .port__body {
      display: flex;
      flex-wrap: nowraps;
      div {
        &:first-child {
          width: 50px;
          height: 50px;
          border-radius: 50%;
          background-color: #ddd;
          overflow: hidden;
        }
        &:last-child {
          position: relative;
          top: -5px;
          text-align: left;
          margin-left: 10px;
          > h4 {
            font-size: 20px;
          }
          > p {
            font-size: 16px;
            color: #2c3a4b;
          }
        }
      }
    }
  }
}
</style>
