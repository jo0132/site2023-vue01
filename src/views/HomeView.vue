<template>
  <main>
    <SliderSection attr="slider__wrap section NanumSquareNeo5" />
    <IntroSection attr="intro__wrap section bg--blue" />
    <PortSection attr="port__wrap section center " />
    <YoutubeSection attr="youtube__wrap section" />
    <UnsplashSection attr="unsplash__wrap section bg--blue" />
    <MovieSection attr="movies__wrap section" />
  </main>
</template>

<script>
// @ is an alias to /src
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";

export default {
  components: {
    IntroSection,
    SliderSection,
    PortSection,
    MovieSection,
    UnsplashSection,
    YoutubeSection,
  },
};
</script>
