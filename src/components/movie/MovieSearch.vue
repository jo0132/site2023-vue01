<template>
  <div class="movies__search container">
    <h2 class="blind">검색하기</h2>
    <input
      ref="inputRef"
      type="search"
      @keypress="onKeyPress"
      placeholder="영화를 검색하세요!"
    />
    <button type="submit" @click="onClick">검색하기</button>
  </div>
</template>

<script>
export default {
  name: "MovieSearch",
  mounted() {
    this.inputRef = this.$refs.inputRef;
  },
  methods: {
    handleSearch() {
      const value = this.inputRef.value;
      this.$emit("on-search", value);
    },
    onKeyPress(event) {
      if (event.key === "Enter") {
        this.handleSearch();
      }
    },
    onClick() {
      this.handleSearch();
    },
  },
  data() {
    return {
      inputRef: null,
    };
  },
};
</script>

<style lang="scss">
.movies__search {
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
    @include button(#f0831e, #fff);
    border-radius: 50px; //bdrs
  }
}
</style>
