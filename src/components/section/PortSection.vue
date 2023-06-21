<template>
  <section id="portSection" :class="attr">
    <h3>한국인이 좋아하는 외국소설</h3>
    <p>그동안 한국인들이 좋아하는 외국 소설입니다.</p>
    <div class="port__inner container">
      <div class="port__btn">
        <ul>
          <li class="active"><a href="#">프랑스</a></li>
          <li><a href="#">미국</a></li>
          <li><a href="#">영국</a></li>
          <li><a href="#">일본</a></li>
        </ul>
      </div>
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
          img: "./assets/images/port/book01.png",
          title: "고양이",
          desc: "베르나르 베르베르",
          icon: "./assets/images/member/peep-27-1.svg",
        },
        {
          img: "./assets/images/port/book02.png",
          title: "파피용",
          desc: "베르나르 베르베르",
          icon: "./assets/images/member/peep-27-1.svg",
        },
        {
          img: "./assets/images/port/book03.png",
          title: "제3인류",
          desc: "베르나르 베르베르",
          icon: "./assets/images/member/peep-27-1.svg",
        },
        {
          img: "./assets/images/port/book04.png",
          title: "당신거기 있어줄래요?",
          desc: "기욤 뮈소",
          icon: "./assets/images/member/peep-54.svg",
        },
        {
          img: "./assets/images/port/book05.png",
          title: "구해줘",
          desc: "기욤 뮈소",
          icon: "./assets/images/member/peep-54.svg",
        },
        {
          img: "./assets/images/port/book06.png",
          title: "센 강의 이름모를 여인",
          desc: "기욤 뮈소",
          icon: "./assets/images/member/peep-54.svg",
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
.port__inner {
  .port__btn {
    > ul {
      margin-bottom: 40px;
      > li {
        display: inline-block;
        width: 126px;
        height: 48px;
        border-radius: 50px;
        background-color: #eaf0ff;
        border: 1px solid #d9e4ff;
        padding: 7px;
        margin-right: 10px;
        &.active {
          display: inline-block;
          width: 126px;
          height: 48px;
          border-radius: 50px;
          background-color: #d9e4ff;
          border: 1px solid #a2bcff;
          padding: 7px;
          color: #666;
        }
        &:hover {
          display: inline-block;
          width: 126px;
          height: 48px;
          border-radius: 50px;
          background-color: #d9e4ff;
          border: 1px solid #a2bcff;
          padding: 7px;
          color: #666;
        }
        > a {
          font-size: 20px;
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
}
</style>
