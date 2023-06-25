<template>
  <ContTitle title="youtude" />
  <YoutubeSlider :youtubes="youtubes" />
  <YoutubeSearch @onSearch="search" />
  <YoutubeTag @onSearch="search" />
  <YoutubeCont :youtubes="youtubes" />
</template>

<script>
// @ is an alias to /src
import ContTitle from "@/components/layout/ContTitle.vue";
import YoutubeSlider from "@/components/youtube/YoutubeSlider.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    YoutubeSlider,
    YoutubeSearch,
    YoutubeTag,
    YoutubeCont,
  },
  setup() {
    const youtubes = ref([]);

    const search = async (query) => {
      try {
        const response = await fetch(
          `https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=30&q=${query}&type=video&key=AIzaSyD52jhFvem-G1E36FNmbTjmruaB8jtIt7M`
        );
        const result = await response.json();
        youtubes.value = result.items;
      } catch (error) {
        console.log("error", error);
      }
    };

    const Toyoutubes = async () => {
      await fetch(
        "https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=30&q=%EC%B1%85%EC%9D%BD%EC%96%B4%EC%A3%BC%EB%8A%94%EB%82%A8%EC%9E%90%20%EA%B8%B0%EC%9A%A4%EB%AE%88%EC%86%8C&type=video&key=AIzaSyD52jhFvem-G1E36FNmbTjmruaB8jtIt7M"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          youtubes.value = result.items;
        })
        .catch((err) => console.error("error", err));
    };
    Toyoutubes();
    return {
      youtubes,
      Toyoutubes,
      search,
    };
  },
};
</script>
