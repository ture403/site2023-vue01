<template>
  <HeaderCont />
  <router-view />
  <FooterrCont />
</template>

<script>
// @ is an alias to /src
import HeaderCont from "@/components/layout/HeaderCont.vue";
import FooterrCont from "@/components/layout/FooterrCont.vue";

export default {
  name: "HomeView",
  components: {
    HeaderCont,
    FooterrCont,
  },
};
</script>
