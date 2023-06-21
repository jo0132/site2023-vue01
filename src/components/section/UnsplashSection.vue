<template>
  <section id="unsplashSection" :class="attr">
    <div class="unsplash__inner container">
      <div class="text">
        <h3>UNSPLASH</h3>
        <p>
          더 다양한 이미지는는 unsplash를 통해 제공하고 있습니다.<br />방문하셔서
          더많은 이미지를 만나보세요!
        </p>
        <a href="#" class="button_bule">자세히 보기</a>
      </div>
      <div class="unsplash__item">
        <div>
          <img
            src="@/assets/images/unsplash/unsplash07.png"
            alt="언스플리쉬 이미지07"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplash08.png"
            alt="언스플리쉬 이미지08"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplash09.png"
            alt="언스플리쉬 이미지09"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplash10.png"
            alt="언스플리쉬 이미지10"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplash11.png"
            alt="언스플리쉬 이미지11"
          />
        </div>
        <div>
          <img
            src="@/assets/images/unsplash/unsplash12.png"
            alt="언스플리쉬 이미지12"
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
.unsplash__wrap {
  background-color: var(--bg_section);
  overflow: hidden;
}
.unsplash__inner {
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
  .unsplash__item {
    @include flex-between;
    margin-top: 70px;
    position: absolute;
    margin-bottom: 100px;
    > div {
      width: 450px;
      margin-right: 20px;
      > img {
        width: 100%;
      }
    }
  }
}

.Unsplash__page {
}
.Unsplash__slider {
  display: none;
}
.Unsplash__search {
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
.Unsplash_tag {
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
.Unsplash_cont {
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
