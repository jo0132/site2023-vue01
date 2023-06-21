<template>
  <section id="moviesSection" :class="attr">
    <div class="movies__inner container">
      <div class="text">
        <h3>MOVIES</h3>
        <p>책을 원작으로 한 영화가 있습니다. 더많은 영화를를 만나보세요!</p>
        <a href="#" class="button_orenge">자세히 보기</a>
      </div>
      <div class="movies__item">
        <div>
          <img src="@/assets/images/movie/movies07.png" alt="영화 이미지07" />
        </div>
        <div>
          <img src="@/assets/images/movie/movies08.png" alt="영화 이미지08" />
        </div>
        <div>
          <img src="@/assets/images/movie/movies09.png" alt="영화 이미지09" />
        </div>
        <div>
          <img src="@/assets/images/movie/movies10.png" alt="영화 이미지10" />
        </div>
        <div>
          <img src="@/assets/images/movie/movies11.png" alt="영화 이미지11" />
        </div>
        <div>
          <img src="@/assets/images/movie/movies12.png" alt="영화 이미지12" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
};
</script>

<style lang="scss">
.movies__wrap {
  overflow: hidden;
}
.movies__inner {
  height: 970px;
  position: relative;
  .text {
    > h3 {
      font-size: 50px;
      font-weight: 700;
      margin-bottom: 50px;
    }
    > p {
      font-size: 22px;
      font-weight: 300;
      margin-bottom: 28px;
    }
    > a {
      border-radius: 50px;
      margin-bottom: 60px;
    }
  }
  .movies__item {
    @include flex-between;
    margin-top: 70px;
    position: absolute;
    margin-bottom: 100px;

    > div {
      width: 350px;
      margin-right: 20px;
      > img {
        width: 100%;
      }
    }
  }
}

.Movie__page {
}
.Movie__slider {
  display: none;
}
.Movie__search {
  text-align: center;
  margin-bottom: 50px;
  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 12px 20px;
    border-radius: 50px;
    min-width: 300px;
    margin-right: 10px;
  }
  button {
    @include button(#f7100d, #fff);
    border-radius: 50px; //bdrs
  }
}
.Movie_tag {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 100px;
    margin-bottom: 60px;
    li {
      a {
        border: 1px solid #f7100d;
        padding: 10px 20px;
        margin: 0 10px;
        color: #f7100d;
      }
    }
  }
}
.Movie_cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 18%;
      margin-bottom: 4%;
    }
    span {
      display: block;
      margin: 4px 0;
    }
  }
}
</style>
