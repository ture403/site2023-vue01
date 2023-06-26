<template>
  <ContTitle title="intro" />
  <IntroText />
</template>
<script>
import IntroText from "@/components/intro/IntroText.vue";
import ContTitle from "@/components/layout/ContTitle.vue";

export default {
  name: "HomeView",
  components: { ContTitle, IntroText },
};
</script>
