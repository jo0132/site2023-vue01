<template>
  <section id="sliderSection" :class="attr">
    <div class="slider__inner">
      <h2 class="blind">이미지 슬라이더</h2>

      <swiper
        :slides-per-view="1"
        :space-between="50"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
        :autoplay="{
          delay: 3000,
          disableOnInteraction: false,
        }"
        :modules="modules"
      >
        <swiper-slide v-for="(slider, index) in sliders" :key="index">
          <div class="slider__img">
            <div class="slider s1 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p v-html="slider.desc"></p>
                <a href="#" class="more button_orenge">더 알아보기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconimage1" :alt="slider.title" />
                <img :src="slider.iconimage2" :alt="slider.title" />
                <img :src="slider.iconimage3" :alt="slider.title" />
              </div>
              <div class="circle">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script>
import { Autoplay } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

export default {
  props: {
    attr: String,
  },
  data: function () {
    return {
      sliders: [
        {
          title: "NEW <br />portfolio",
          desc: "더 많이 읽을수록, 더 많은 것을 알게 됩니다.<br />더 많이 배울수록, 더 많은 곳에 갈 수 있습니다.",
          iconimage1: "./assets/images/slider/slider01.png",
          iconimage2: "./assets/images/slider/slider02.png",
          iconimage3: "./assets/images/slider/slider03.png",
        },
        {
          title: "NEW <br />portfolio",
          desc: "더 많이 읽을수록, 더 많은 것을 알게 됩니다.<br />더 많이 배울수록, 더 많은 곳에 갈 수 있습니다.",
          iconimage1: "./assets/images/slider/slider01.png",
          iconimage2: "./assets/images/slider/slider02.png",
          iconimage3: "./assets/images/slider/slider03.png",
        },
        {
          title: "NEW <br />portfolio",
          desc: "더 많이 읽을수록, 더 많은 것을 알게 됩니다.<br />더 많이 배울수록, 더 많은 곳에 갈 수 있습니다.",
          iconimage1: "./assets/images/slider/slider01.png",
          iconimage2: "./assets/images/slider/slider02.png",
          iconimage3: "./assets/images/slider/slider03.png",
        },
      ],
    };
  },
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
      modules: [Autoplay],
    };
  },
  methods: {},
};
</script>

<style lang="scss">
.swiper {
  overflow: visible;
}
.swiper-pagination {
  bottom: -80px !important;
}
.slider__wrap {
  // background-color: rgba(0,0,0,0.1);
}
.slider__inner {
  position: relative;
  overflow: hidden;
  padding: 70px 0;
  .slider__img {
    .slider {
      .text {
        h3 {
          font-size: 110px;
          font-weight: 800;
          text-transform: uppercase;
          line-height: 1;
          margin-bottom: 40px;
        }
        p {
          font-size: 24px;
          font-weight: 500;
          margin-bottom: 50px;
        }
        .more {
          font-size: 18px;
        }
      }
      .img {
        position: absolute;
        right: 0;
        top: -120px;
        width: 600px;
        height: 600px;
        background-image: url(@/assets/images/slider/circle.png);
        background-size: cover;
        background-position: center;
        & img:nth-child(1) {
          position: absolute;
          width: 250px;
          left: -30px;
          transform: rotate(-25deg);
        }
        & img:nth-child(2) {
          position: absolute;
          width: 250px;
          right: 0;
          top: 50px;
        }
        & img:nth-child(3) {
          position: absolute;
          width: 250px;
          bottom: 0;
          left: 50px;
        }
      }
      .circle {
        span {
          display: block;
          position: absolute;
          left: 50%;
          top: 50%;
          width: 20px;
          height: 20px;
          border-radius: 50%;
        }
        span:nth-child(1) {
          background-color: var(--button_orenge);
          left: 40%;
          top: 60%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(2) {
          background-color: var(--button_vie);
          top: 50%;
          width: 40px;
          height: 40px;
        }
        span:nth-child(3) {
          background-color: var(--button_bule);
          left: 100%;
          width: 30px;
          height: 30px;
        }
        span:nth-child(4) {
          background-color: var(--button_orenge);
          left: 20%;
          top: -10%;
        }
        span:nth-child(5) {
          background-color: var(--button_vie);
          left: -10%;
          top: 20%;
        }
      }
    }
  }
  .slider__btn {
    > a {
      position: absolute;
      width: 25px;
      height: 40px;
      top: 50%;
      background-repeat: no-repeat;
      background-position: center;
      transform: translateY(-50%);
      transition: opacity 0.3s;
      &:hover {
        opacity: 0.5;
      }
    }
    .left {
      left: 20px;
      background-image: url(@/assets/images/slider/sliderLeft.png);
    }
    .right {
      right: 20px;
      background-image: url(@/assets/images/slider/sliderRight.png);
    }
  }
  .slider__dot {
    position: absolute;
    left: 50%;
    bottom: -80px;
    transform: translateX(-50%);
    a {
      display: inline-block;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      margin: 0 5px;
      border: 4px solid #ff3344;
      background-color: #ff3344;
      box-shadow: 0 0 0 3px transparent;
      transition: all 0.3s;
      &.active {
        box-shadow: 0 0 0 3px #ff3344;
        border-width: 4px;
        background-color: #fff;
      }
      &:hover {
        transform: scale(1.2);
      }
    }
  }
}
</style>
