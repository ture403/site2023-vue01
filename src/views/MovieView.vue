<template>
  <div>
    <ContTitle title="movies" />
    <MovieSlider :movies="movies" />
    <MovieSearch />
    <MovieTag />
    <MovieCont :movies="movies" />
  </div>
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieSearch from "@/components/movie/MovieSearch.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";
import { ref } from "vue";

export default {
  name: "HomeView",
  components: {
    ContTitle,
    MovieSlider,
    MovieSearch,
    MovieTag,
    MovieCont,
  },

  setup() {
    const movies = ref([]);
    const searchs = ref([]);
    const search = ref("marvel");

    const TopMovies = async () => {
      await fetch(
        `https://api.themoviedb.org/3/movie/popular?api_key=76bdc971ba84bff496ab1d4f27cc9c5c&query=${search.value}`
      )
        .then((response) => response.json())
        .then((result) => {
          movies.value = result.results;
          searchs.value = result.results;
        })
        .catch((error) => console.log("error", error));
    };
    TopMovies();
    return {
      searchs,
      movies,
      TopMovies,
    };
  },
};
</script>
