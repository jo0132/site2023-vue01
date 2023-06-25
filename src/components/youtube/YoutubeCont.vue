<template>
  <div class="Youtube_cont Youtube__page container">
    <ul>
      <li v-for="(youtube, index) in youtubes" :key="index">
        <a :href="`https://youtu.be/${youtube.id.videoId}`">
          <img
            :src="youtube.snippet.thumbnails.medium.url"
            :alt="youtube.snippet.title"
          />
          <span>{{ youtube.snippet.title }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.Youtube_cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 24%;
      margin-bottom: 4%;
    }
    > img {
    }
    span {
      display: block;
      margin: 4px 0;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
      -webkit-line-clamp: 1; /* 라인수 */
      -webkit-box-orient: vertical;
      word-wrap: break-word;
    }
  }
}
</style>
