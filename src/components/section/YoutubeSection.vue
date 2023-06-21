<template>
  <section id="youtubeSection" :class="attr">
    <div class="youtube__inner container">
      <div class="text">
        <h3>YOUTUBE</h3>
        <p>
          바쁜 분들을 위해 책을 읽어주는 유투버들이 있습니다.<br />방문하시고
          구독과 좋아요! 부탁드립니다.
        </p>
        <a href="#" class="button_vie">자세히 보기</a>
      </div>
      <div class="youtube__item">
        <div>
          <img
            src="@/assets/images/youtube/youtube07.png"
            alt="유투브 이미지07"
          />
        </div>
        <div>
          <img
            src="@/assets/images/youtube/youtube08.png"
            alt="유투브 이미지08"
          />
        </div>
        <div>
          <img
            src="@/assets/images/youtube/youtube09.png"
            alt="유투브 이미지09"
          />
        </div>
        <div>
          <img
            src="@/assets/images/youtube/youtube10.png"
            alt="유투브 이미지10"
          />
        </div>
        <div>
          <img
            src="@/assets/images/youtube/youtube11.png"
            alt="유투브 이미지11"
          />
        </div>
        <div>
          <img
            src="@/assets/images/youtube/youtube12.png"
            alt="유투브 이미지12"
          />
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
.youtube__wrap {
  overflow: hidden;
}
.youtube__inner {
  height: 700px;
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
  .youtube__item {
    @include flex-between;
    margin-top: 70px;
    margin-bottom: 120px;
    position: absolute;
    > div {
      width: 450px;
      margin-right: 20px;
      > img {
        width: 100%;
      }
    }
  }
}

.Youtube__page {
}
.Youtube__slider {
  display: none;
}
.youtube__search {
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
.Youtube_tag {
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
.Youtube_cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 31.333%;
      margin-bottom: 4%;
    }
    span {
      display: block;
      margin: 4px 0;
    }
  }
}
</style>
