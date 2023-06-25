<template>
  <div class="movie__tag container">
    <ul>
      <li>
        <a @click="onClick('10749')">로맨스영화</a>
      </li>
      <li>
        <a @click="onClick('28')">액션영화</a>
      </li>
      <li>
        <a @click="onClick('35')">코미디영화</a>
      </li>
      <li>
        <a @click="onClick('16')">애니메이션</a>
      </li>
      <li>
        <a @click="onClick('27')">공포영화</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    onClick(value) {
      this.$emit("on-search", value);
    },
  },
};
</script>

<style lang="scss">
.movie__tag {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 100px;
    margin-bottom: 60px;
    li {
      a {
        border: 1px solid #da6900;
        padding: 10px 20px;
        margin: 0 10px;
        color: #da6900;
        border-radius: 50px;
      }
      :hover {
        background-color: #da6900;
        color: #fff;
      }
    }
  }
}
</style>
