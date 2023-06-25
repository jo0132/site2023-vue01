<template>
  <section id="portSection" :class="attr">
    <h3>한국인이 좋아하는 외국소설</h3>
    <p>그동안 한국인들이 좋아하는 외국 소설입니다.</p>
    <div class="port__inner container">
      <div class="port__cont">
        <div class="port" v-for="(text, index) in texts" :key="index">
          <figure class="port__header">
            <img :src="text.img" :alt="text.title" />
          </figure>
          <div class="port__body">
            <div class="pic">
              <img :src="text.icon" :alt="text.desc" />
            </div>
            <div>
              <h4>{{ text.title }}</h4>
              <p>{{ text.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      texts: [
        {
          img: "../assets/images/port/기욤뮈소01.png",
          icon: "../assets/images/member/peep-54.svg",
          title: "당신거기 있어줄래요?",
          desc: "기욤 뮈소",
        },
        {
          img: "../assets/images/port/기욤뮈소02.png",
          icon: "../assets/images/member/peep-54.svg",
          title: "구해줘",
          desc: "기욤 뮈소",
        },
        {
          img: "../assets/images/port/기욤뮈소03.png",
          icon: "../assets/images/member/peep-54.svg",
          title: "센 강의 이름모를 여인",
          desc: "기욤 뮈소",
        },
        {
          img: "../assets/images/port/기욤뮈소04.png",
          icon: "../assets/images/member/peep-54.svg",
          title: "종이 여자",
          desc: "기욤 뮈소",
        },
        {
          img: "../assets/images/port/기욤뮈소05.png",
          icon: "../assets/images/member/peep-54.svg",
          title: "안젤리크",
          desc: "기욤 뮈소",
        },
        {
          img: "../assets/images/port/기욤뮈소06.png",
          icon: "../assets/images/member/peep-54.svg",
          title: "작가들의 비밀스러운 삶",
          desc: "기욤 뮈소",
        },
      ],
    };
  },
  props: {
    attr: String,
  },
};
</script>

<style lang="scss">
//port__wrap
.port__wrap {
  background-color: var(--bg_section);
}
.port__btn {
  > ul {
    margin-bottom: 40px;
    text-align: center;
    > li {
      display: inline-block;
      width: 200px;
      height: 48px;
      border-radius: 50px;
      background-color: #e9eeff;
      border: 1px solid #2250c5;
      padding: 7px;
      margin-right: 10px;
      color: #fff;
      &.active {
        display: inline-block;
        width: 200px;
        height: 48px;
        border-radius: 50px;
        background-color: #b7cbfd;
        border: 1px solid #092d88;
        padding: 7px;
        color: #fff;
      }
      &:hover {
        display: inline-block;
        width: 200px;
        height: 48px;
        border-radius: 50px;
        background-color: #2250c5;
        border: 1px solid #092d88;
        padding: 7px;
        color: #fff;
      }
      > a {
        font-size: 20px;
        color: #fff;
      }
    }
  }
}
.port__cont {
  @include flex-between;
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
