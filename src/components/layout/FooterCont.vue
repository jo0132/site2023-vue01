<template>
  <footer
    id="footer"
    class="footer__wrap section bg--blue NanumSquareNeo5"
    aria-level="1"
  >
    <div class="footer__inner container">
      <div class="footer__text">
        <h5>노지감귤</h5>
        <p>
          궁금한 사항은 <br />
          메일로 연락 주세요!
          <br />
          <RouterLink to="mailto:jo0132@naver.com">jo0132@naver.com</RouterLink>
        </p>
        <ul class="sns">
          <li>
            <RouterLink to="/"> </RouterLink>
          </li>
          <li>
            <RouterLink to="/"> </RouterLink>
          </li>
          <li>
            <RouterLink to="/"> </RouterLink>
          </li>
          <li>
            <RouterLink to="/"> </RouterLink>
          </li>
          <li>
            <RouterLink to="/"> </RouterLink>
          </li>
        </ul>
      </div>
      <div class="footer__menu">
        <div>
          <h4>사이트</h4>
          <ul>
            <li>
              <RouterLink to="/">웹표준 사이트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">반응형 사이트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">패럴랙스 사이트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">포트폴리오 사이트</RouterLink>
            </li>
          </ul>
        </div>
        <div>
          <h4>유형</h4>
          <ul>
            <li>
              <RouterLink to="/">이미지 유형</RouterLink>
            </li>
            <li>
              <RouterLink to="/">카드 유형</RouterLink>
            </li>
            <li>
              <RouterLink to="/">이미지/텍스트 유형</RouterLink>
            </li>
            <li>
              <RouterLink to="/">텍스트 유형</RouterLink>
            </li>
            <li>
              <RouterLink to="/">베너 유형</RouterLink>
            </li>
            <li>
              <RouterLink to="/">푸터 유형</RouterLink>
            </li>
          </ul>
        </div>
        <div>
          <h4>스크립트</h4>
          <ul>
            <li>
              <RouterLink to="/">검색 이팩트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">퀴즈 이팩트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">마우스 이팩트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">슬라이드 이팩트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">페럴랙스 이팩트</RouterLink>
            </li>
            <li>
              <RouterLink to="/">게임 이팩트</RouterLink>
            </li>
          </ul>
        </div>
        <div>
          <h4>언어</h4>
          <ul>
            <li>
              <RouterLink to="/">CSS</RouterLink>
            </li>
            <li>
              <RouterLink to="/">HTML</RouterLink>
            </li>
            <li>
              <RouterLink to="/">JAVASCRIPT</RouterLink>
            </li>
            <li>
              <RouterLink to="/">REACT</RouterLink>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__right">
        Copyright 2023. All Rights Reserved. - Designed by noji감귤
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
.footer__wrap {
  background-color: var(--bg_section);
}
.footer__inner {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  .footer__text {
    width: 30%;
    > h5 {
      font-size: 18px;
      margin-bottom: 25px;
    }
    > p {
      font-size: 14px;
      color: #808080;
      margin-bottom: 25px;
      > a {
        color: #808080;
      }
    }
    > ul {
      display: flex;
      li {
        width: 45px;
        height: 45px;
        border-radius: 50px;
        background-color: #f5f5f5;
        margin-right: 10px;
        &:nth-child(1) {
          width: 45px;
          height: 45px;
          background-repeat: no-repeat;
          background-position: center center;
          background-size: 25px;
          background-image: url(@/assets/images/footer/Instagram.png);
        }
        &:nth-child(2) {
          width: 45px;
          height: 45px;
          width: 45px;
          height: 45px;
          background-repeat: no-repeat;
          background-position: center center;
          background-size: 25px;
          background-image: url(@/assets/images/footer/YouTube.png);
        }
        &:nth-child(3) {
          width: 45px;
          height: 45px;
          width: 45px;
          height: 45px;
          background-repeat: no-repeat;
          background-position: center center;
          background-size: 25px;
          background-image: url(@/assets/images/footer/Link-1.png);
        }
        &:nth-child(4) {
          width: 45px;
          height: 45px;
          width: 45px;
          height: 45px;
          background-repeat: no-repeat;
          background-position: center center;
          background-size: 25px;
          background-image: url(@/assets/images/footer/Link.png);
        }
        &:nth-child(5) {
          width: 45px;
          height: 45px;
          width: 45px;
          height: 45px;
          background-repeat: no-repeat;
          background-position: center center;
          background-size: 25px;
          background-image: url(@/assets/images/footer/Facebook.png);
        }
      }
    }
  }
  .footer__menu {
    width: 70%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 50px;
    > div {
      width: 25%;
      > h4 {
        font-size: 18px;
        color: #000;
        margin-bottom: 24px;
      }
      > ul {
        li {
          a {
            color: #808080;
            margin-bottom: 13px;
          }
        }
      }
    }
  }
  .footer__right {
    padding-top: 50px;
    border-top: 1px solid #e6e6e6;

    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
.footer__wrap {
}
</style>
