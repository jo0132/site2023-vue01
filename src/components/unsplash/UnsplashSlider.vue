<template>
  <div class="unsplash__slider">
    <swiper
      :modules="modules"
      :autoplay="{ delay: 2000, disableOnInteraction: true }"
      :spaceBetween="30"
      effect="fade"
      :navigation="true"
      :pagination="{ clickable: true }"
      class="mySwiper"
    >
      <swiper-slide v-for="(image, index) in images" :key="index">
        <a :href="`https://unsplash.com/photos/${image.id}`" target="_blank">
          <img :src="image.urls.regular" :alt="image.alt_description" />
        </a>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
// import Swiper core and required modules
// import Swiper from "swiper";
import { EffectFade, Autoplay, Navigation, Pagination } from "swiper";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

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
    images: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang="scss">
.unsplash__slider {
  margin-bottom: 160px;
  a {
    img {
      width: 100%;
      height: 500px;
      object-fit: cover;
    }
  }
}
</style>
