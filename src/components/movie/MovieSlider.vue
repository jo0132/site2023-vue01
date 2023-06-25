<template>
  <div class="movie__slider">
    <swiper
      :modules="modules"
      :slides-per-view="2"
      :spaceBetween="30"
      effect="fade"
      :navigation="true"
      :pagination="{ clickable: true }"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
      :autoplay="{ delay: 4000 }"
    >
      <swiper-slide v-for="(movie, index) in movies" :key="index">
        <a :href="`https://www.themoviedb.org/movie/${movie.id}`">
          <img
            :src="`https://image.tmdb.org/t/p/original${movie.backdrop_path}`"
            :alt="movie.title"
          />
        </a>
        <div class="desc Rebecca">
          <h1 v-if="movie.original_title">{{ movie.original_title }}</h1>
          <h1 v-else>{{ movie.original_name }}</h1>
          <p class="SeoulHangang3">{{ movie.overview }}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// import Swiper core and required modules
import { EffectFade, Navigation, Pagination, Autoplay } from "swiper";

// Import Swiper styles
import "swiper/css";
import "swiper/scss/navigation";
import "swiper/scss/pagination";
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
      modules: [EffectFade, Autoplay, Navigation, Pagination],
    };
  },
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.movie__slider {
  margin-bottom: 120px;
  position: relative;
  a {
    display: inline-block;
    width: 100%;
    height: 800px;
    object-fit: cover;
    img {
      width: 100%;
      height: 800px;
      object-fit: cover;
    }
  }
  .desc {
    position: absolute;
    background: linear-gradient(
      to bottom,
      #00000000 0%,
      #0000007a 70%,
      #000000 100%
    );
    color: #fff;
    width: 100%;
    height: 400px;
    bottom: 0;
    padding: 100px 25px;

    > h1 {
      display: inline-block;
      padding: 10px 20px 20px;
      font-size: 3vw;
      font-weight: bold;
      border-left: 20px solid #fff;
    }

    p {
      border-left: 20px solid #fff;
      padding: 20px;
      width: 60%;
      white-space: normal;
      line-height: 1.2;
      height: 100px;
      text-align: left;
      word-wrap: break-word;
      -webkit-line-clamp: 3;
      -webkit-box-orient: vertical;
      letter-spacing: 0.5px;
    }
  }
}
</style>
