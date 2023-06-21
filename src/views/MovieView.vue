<template>
  <ContTitle />
  <MovieSlider />
  <MovieSearch />
  <MovieTag />
  <MovieCont />
</template>

<script>
// @ is an alias to /src
import ContTitle from "@/components/layout/ContTitle.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";

export default {
  components: {
    ContTitle,
    MovieSlider,
    MovieSearch,
    MovieTag,
    MovieCont,
  },
};
</script>
