<template>
  <div>
    <ContTitle title="Unsplash" />
    <UnsplashSlider :images="images" />
    <UnsplashSearch @onSearch="search" />
    <UnsplashTag @onSearch="search" />
    <UnsplashCont :images="images" />
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import { ref } from "vue";

export default {
  name: "UnsplashPage",
  components: {
    ContTitle,
    UnsplashSlider,
    UnsplashSearch,
    UnsplashTag,
    UnsplashCont,
  },
  setup() {
    const images = ref([]);

    const search = async (query) => {
      try {
        const response = await fetch(
          `https://api.unsplash.com/search/photos?client_id=EKtMJsPkvjN9rFiXwrOAQN79zIJbkkXkTuqD5SAhqU0&per_page=30&query=${query}`
        );
        const result = await response.json();
        images.value = result.results;
      } catch (error) {
        console.log("error", error);
      }
    };
    const ToImages = async () => {
      await fetch(
        "https://api.unsplash.com/photos?client_id=EKtMJsPkvjN9rFiXwrOAQN79zIJbkkXkTuqD5SAhqU0&per_page=30"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          images.value = result;
        })
        .catch((err) => console.error("error", err));
    };
    ToImages();
    return {
      images,
      ToImages,
      search,
    };
  },
};
</script>

<style lang="scss">
.unsplash__cont {
  ul {
    column-count: 4;
    column-gap: 20px;
    li {
      margin-bottom: 20px;
    }
  }
}
</style>
