<template>
  <div class="Youtube_tag">
    <div>
      <button @click="onClick('기욤뮈소')">기욤뮈소</button>
      <button @click="onClick('j.k 롤링')">j.k 롤링</button>
      <button @click="onClick('베르나르베르베르')">베르나르베르베르</button>
      <button @click="onClick('히가시노 게이고')">히가시노 게이고</button>
      <button @click="onClick('댄브라운')">댄브라운</button>
      <button @click="onClick('댄브라운')">댄브라운</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    onClick(value) {
      this.$emit("onSearch", value);
    },
  },
};
</script>
<style lang="scss">
.Youtube_tag {
  div {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 100px;
    margin-bottom: 60px;
    button {
      border: 1px solid #f0831e;
      padding: 10px 20px;
      margin: 0 10px;
      color: #f0831e;
      border-radius: 50px;
    }
    :hover {
      background-color: #f0831e;
      color: #fff;
    }
  }
}
</style>
