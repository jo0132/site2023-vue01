<template>
  <HeaderCont />
  <router-view />
  <FooterCont />
</template>

<script>
// @ is an alias to /src
import HeaderCont from "@/components/layout/HeaderCont.vue";
import FooterCont from "@/components/layout/FooterCont.vue";

export default {
  components: {
    HeaderCont,
    FooterCont,
  },
};
</script>

<style lang="scss">
@import "style.scss";
</style>
