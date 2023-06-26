<template>
  <div>
    <ContTitle title="unsplash" />
    <UnsplashSlider :unsplashs="unsplashs" />
    <UnsplashSearch />
    <UnsplashTag />
    <UnsplashCont :unsplashs="unsplashs" />
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import { ref } from "vue";

export default {
  name: "HomeView",
  components: {
    ContTitle,
    UnsplashSlider,
    UnsplashSearch,
    UnsplashTag,
    UnsplashCont,
  },

  setup() {
    const unsplashs = ref([]);

    const TopUnsplashs = async () => {
      await fetch(
        "https://api.unsplash.com/search/photos?client_id=3fLduMDzaR7Vq59dINrEif7nOY0l0PjeyPwMkrn3Roc&per_page=30&order_by=popular&query=seoul"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          unsplashs.value = result.results;
        })
        .catch((error) => console.log("error", error));
    };
    TopUnsplashs();
    return {
      unsplashs,
      TopUnsplashs,
    };
  },
};
</script>
