<template>
  <div class="unsplash__search container">
    <h2 class="blind">검색하기</h2>
    <input
      ref="inputRef"
      type="search"
      @keypress="onKeyPress"
      placeholder="이미지를 검색하세요!"
    />
    <button type="submit" @click="onClick">검색하기</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "UnsplashSearch",
  setup(props, { emit }) {
    const inputRef = ref(null);

    const handleSearch = () => {
      const value = inputRef.value.value;
      emit("onSearch", value);
    };

    const onKeyPress = (event) => {
      if (event.key === "Enter") {
        handleSearch();
      }
    };

    const onClick = () => {
      handleSearch();
    };

    return {
      inputRef,
      onKeyPress,
      onClick,
    };
  },
};
</script>
<style lang="scss">
.unsplash__search {
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
