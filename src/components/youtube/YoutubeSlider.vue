<template>
  <div class="youtube__slider">
    <swiper
      :modules="modules"
      :autoplay="{ delay: 1000, disableOnInteraction: true }"
      effect="coverflow"
      :grabCursor="true"
      :centeredSlides="true"
      :slidesPerView="5"
      :coverflowEffect="{
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: true,
      }"
      :pagination="true"
      class="mySwiper"
    >
      <SwiperSlide v-for="(youtube, index) in youtubes" :key="index">
        <a :href="`https://youtu.be/${youtube.id.videoId}`" target="_blank">
          <img
            :src="youtube.snippet.thumbnails.medium.url"
            :alt="youtube.snippet.title"
          />
        </a>
      </SwiperSlide>
    </swiper>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// import Swiper core and required modules
import { EffectCoverflow, Navigation, Pagination, Autoplay } from "swiper";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/effect-coverflow";

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
      modules: [EffectCoverflow, Autoplay, Navigation, Pagination],
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
.youtube__slider {
  margin-bottom: 160px;
  a {
    img {
      height: 100%;
      width: 100%;
      object-fit: cover;
    }
  }
}
</style>
