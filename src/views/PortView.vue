<template>
  <ContTitle title="gallery" />
  <PortText />
</template>
<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import PortText from "@/components/port/PortText.vue";

export default {
  name: "HomeView",
  components: {
    ContTitle,
    PortText,
  },
};
</script>
