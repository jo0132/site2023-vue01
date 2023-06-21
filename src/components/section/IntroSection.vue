<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">사이트 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>frontend</span>
        <h3 v-html="title"></h3>
        <p v-html="desc"></p>
      </div>
      <div class="intro__desc">
        <div v-for="(text, index) in texts" :key="index">
          <h4 v-bind:class="'icon-bg' + (index + 1)">{{ text.title }}</h4>
          <p>
            {{ text.desc }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      title: `외국 소설들을<br />소개합니다.`,
      desc: `저희 사이트는 여러분의 사랑을 받는 소설을<br /> 소개하는 사이트 입니다.<br /> 그 전에 좋은 소설을 찾는 것이 중요합니다.`,
      texts: [
        {
          title: "장르와 관심사 파악",
          desc: "자신이 선호하는 장르나 관심사를 고려하여 독서목록을 작성해 보세요. 이를 통해 원하는 주제나 스타일의 소설을 찾을 수 있습니다.",
        },
        {
          title: "베스트셀러 목록 확인",
          desc: "베스트셀러 목록은 대중적인 인기를 얻은 소설들을 포함하고 있습니다. 출판사나 온라인 서점의 베스트셀러 목록을 확인해보면 다양한 장르와 주제의 인기 작품을 찾을 수 있습니다.",
        },
        {
          title: "작가의 다른 작품 탐색",
          desc: "이미 좋아하는 작가의 다른 작품을 찾아보세요. 작가의 스타일이나 이야기 구성에 대한 선호도가 유사할 가능성이 큽니다.",
        },
        {
          title: "도서관 방문",
          desc: "도서관은 다양한 작품을 무료로 대여할 수 있는 좋은 장소입니다. 도서관의 추천 도서나 독서 행사를 확인하여 다양한 소설을 만나보세요.",
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
// intro__wrap
.intro__wrap {
}
.intro__inner {
  display: flex;
  justify-content: space-between;
}
.intro__title {
  width: 33%;
  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }
  h3 {
    font-size: 50px;
    font-weight: 900;
    line-height: 1.2;
    margin-bottom: 30px;
  }
  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}
.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  > div {
    width: 48%;
    margin-bottom: 40px;
    h4 {
      font-size: 24px;
      margin-bottom: 15px;
      display: inline-block;
    }
    &:nth-child(3) {
      margin-bottom: 0;
    }
    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
