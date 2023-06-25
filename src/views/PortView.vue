<template>
  <div>
    <ContTitle title="fiction" />
    <PortCont />
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import PortCont from "@/components/portfolio/PortCont.vue";

export default {
  components: {
    ContTitle,
    PortCont,
  },
};
</script>
