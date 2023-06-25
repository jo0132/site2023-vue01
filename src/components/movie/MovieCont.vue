<template>
  <div class="movies__cont container">
    <ul>
      <li v-for="(movie, index) in movies" :key="index">
        <a
          :href="`https://www.themoviedb.org/movie/${movie.id}`"
          target="_blank"
        >
          <img
            :src="`https://image.tmdb.org/t/p/w300${movie.poster_path}`"
            :alt="movie.title"
          />
          <span class="title">{{ movie.title }}</span>
          <span class="star">{{ movie.vote_average.toFixed(1) }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.movies__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    > li {
      position: relative;
      a {
        .title {
          width: 300px;
          font-size: 20px;
          padding: 3px 0;
          display: inline-block;

          &:hover {
            text-decoration: underline;
            text-underline-position: under;
          }
        }

        .star {
          position: absolute;
          right: 20px;
          top: 20px;
          width: 30px;
          height: 30px;
          background-color: #fff;
          text-align: center;
          line-height: 30px;
          border-radius: 50px;
          font-size: 12px;
        }
      }
    }
  }
}
</style>
