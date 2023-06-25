<template>
  <div class="unsplash_tag">
    <div>
      <button @click="onClick('book')">book</button>
      <button @click="onClick('Genre')">Genre</button>
      <button @click="onClick('Fiction')">Fiction</button>
      <button @click="onClick('Library')">Library</button>
      <button @click="onClick('Author')">Author</button>
      <button @click="onClick('Character')">Character</button>
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
.unsplash_tag {
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
