<template>
  <div className="intro__slider__inner">
    <h2 className="blind">이미지 슬라이더</h2>
    <div class="intro__slider__img">
      <swiper
        :modules="modules"
        :autoplay="{ delay: 2000, disableOnInteraction: true }"
        :spaceBetween="30"
        effect="fade"
        :navigation="true"
        :pagination="{ clickable: true }"
        class="mySwiper"
      >
        <SwiperSlide>
          <img
            src="@/assets/images/intro/intro_slider_img01.jpg"
            alt="인트로 슬라이드 이미지1"
          />
        </SwiperSlide>
        <SwiperSlide>
          <img
            src="@/assets/images/intro/intro_slider_img02.jpg"
            alt="인트로 슬라이드 이미지2"
          />
        </SwiperSlide>
        <SwiperSlide>
          <img
            src="@/assets/images/intro/intro_slider_img03.jpg"
            alt="인트로 슬라이드 이미지3"
          />
        </SwiperSlide>
      </swiper>
    </div>
  </div>
  <div class="intro__cont container">
    <div class="intro__cont__inner right">
      <div class="introPage_desc right_text">
        <h4 class="intro__text__title Rebecca">
          장르와
          <br />
          관심사 파악
        </h4>
        <p class="intro__text__desc SeoulHangang3">
          자신이 선호하는 장르나 관심사를 고려하여 독서목록을 작성해 보세요.
          이를 통해 원하는 주제나 스타일의 소설을 찾을 수 있습니다.
        </p>
        <a class="Rebecca" href="https://www.yes24.com/main/default.aspx">
          찾아보기
        </a>
      </div>
      <div class="introPage_img">
        <img
          class="intro__text__img"
          src="@/assets/images/intro/intro_img01.jpg"
          alt="인트로 이미지1"
        />
      </div>
    </div>
    <div class="intro__cont__inner left">
      <div class="introPage_desc">
        <h4 class="intro__text__title Rebecca">
          베스트셀러
          <br />
          목록 확인
        </h4>
        <p class="intro__text__desc SeoulHangang3">
          베스트셀러 목록은 대중적인 인기를 얻은 소설들을 포함하고 있습니다.
          출판사나 온라인 서점의 베스트셀러 목록을 확인해보면 다양한 장르와
          주제의 인기 작품을 찾을 수 있습니다.
        </p>
        <a class="Rebecca" href="https://www.yes24.com/main/default.aspx">
          찾아보기
        </a>
      </div>
      <div class="introPage_img">
        <img
          class="intro__text__img"
          src="@/assets/images/intro/intro_img02.jpg"
          alt="인트로 이미지2"
        />
      </div>
    </div>
    <div class="intro__cont__inner right">
      <div class="introPage_desc right_text">
        <h4 class="intro__text__title Rebecca">
          작가의
          <br />
          다른 작품 탐색
        </h4>
        <p class="intro__text__desc SeoulHangang3">
          이미 좋아하는 작가의 다른 작품을 찾아보세요. 작가의 스타일이나 이야기
          구성에 대한 선호도가 유사할 가능성이 큽니다.
        </p>
        <a class="Rebecca" href="https://www.yes24.com/main/default.aspx">
          찾아보기
        </a>
      </div>
      <div class="introPage_img">
        <img
          class="intro__text__img"
          src="@/assets/images/intro/intro_img03.jpg"
          alt="인트로 이미지3"
        />
      </div>
    </div>
    <div class="intro__cont__inner left">
      <div class="introPage_desc">
        <h4 class="intro__text__title Rebecca">도서관 방문</h4>
        <p class="intro__text__desc SeoulHangang3">
          도서관은 다양한 작품을 무료로 대여할 수 있는 좋은 장소입니다. 도서관의
          추천 도서나 독서 행사를 확인하여 다양한 소설을 만나보세요.
        </p>
        <a class="Rebecca" href="https://www.yes24.com/main/default.aspx">
          찾아보기
        </a>
      </div>
      <div class="introPage_img">
        <img
          class="intro__text__img"
          src="@/assets/images/intro/intro_img04.jpg"
          alt="인트로 이미지4"
        />
      </div>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// import Swiper core and required modules
import { EffectFade, Autoplay } from "swiper";

// Import Swiper styles
import "swiper/css";

import "swiper/css/effect-fade";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [EffectFade, Autoplay],
    };
  },
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
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

.intro__slider__inner {
  margin-bottom: 120px;
  height: 300px;

  .intro__slider__img {
    img {
      width: 100%;
      height: 300px;
      object-fit: cover;
      position: relative;
    }
  }
}

.intro__cont {
  color: #f0831e;
  .intro__cont__inner {
    display: flex;
    justify-content: space-between;
    margin-bottom: 130px;
  }
  .introPage_desc {
    width: 50%;
    height: 400px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    .intro__text__title {
      font-size: 3vw;
      line-height: 1.5;
    }

    .intro__text__desc {
      width: 60%;
      line-height: 1.5;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    > a {
      color: #f0831e;
      font-size: 1.2vw;
    }
  }
  .introPage_img {
    width: 50%;
    height: 400px;

    .intro__text__img {
      width: 100%;
      height: 400px;
      object-fit: cover;
    }
  }
  .right {
    display: flex;
    flex-direction: row-reverse;
  }
  .right_text {
    text-align: right;
    align-items: flex-end;
  }
}
</style>
