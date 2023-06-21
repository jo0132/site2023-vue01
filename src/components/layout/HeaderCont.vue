<template>
  <header
    id="header"
    class="Header__wrap NanumSquareNeo5"
    role="heading"
    aria-level="1"
  >
    <div class="header__inner container">
      <h1 class="header__logo">
        <RouterLink to="/"> noji <em>감귤</em> </RouterLink>
      </h1>
      <nav class="header__nav" role="navigation">
        <ul>
          <li>
            <RouterLink to="/intro">소개</RouterLink>
          </li>
          <li>
            <RouterLink to="/port">작품</RouterLink>
          </li>
          <li>
            <RouterLink to="/youtube">유튜브</RouterLink>
          </li>
          <li>
            <RouterLink to="/unsplash">이미지</RouterLink>
          </li>
          <li>
            <RouterLink to="/movie">영화</RouterLink>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss">
// header__wrap
.header__wrap {
  // background-color: var(--bg_section);
}
.header__inner {
  text-align: center;
  .header__logo {
    width: 100%;
    font-size: 30px;

    a {
      font-size: 30px;
      display: inline-block;
      padding: 5px;
      margin: 5px;
      text-transform: uppercase;
      font-weight: 800;

      em {
        text-transform: lowercase;
        font-weight: 500;
      }
    }
  }
  .header__nav {
    width: 100%;
    ul {
      padding: 0 10%;
      display: flex;
      justify-content: space-between;

      li {
        a {
          display: inline-block;
          padding: 5px 5px 0 5px;
          margin: 5px 5px 0 5px;
          position: relative;

          &::before {
            content: "";
            width: calc(100% - 20px);
            height: 2px;
            color: var(--color_body);

            position: absolute;
            left: 10px;
            bottom: 4px;
            transform: scaleX(0);
            transition: all 0.3s ease;
          }

          &:hover::before {
            transform: scaleX(1);
          }
        }
      }
    }
  }
}
</style>
