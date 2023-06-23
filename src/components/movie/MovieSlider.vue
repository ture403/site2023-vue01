<template>
  <div className="movie__slider">
    <Swiper
      class="Swiper"
      :modules="modules"
      :slides-per-view="5"
      :space-between="50"
      navigation
      :pagination="{ clickable: true }"
      :autoplay="{
        delay: 5000,
        disableOnInteraction: false,
      }"
      :loop="true"
      :coverflowEffect="{
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: true,
      }"
    >
      <SwiperSlide v-for="(movie, index) in movies" :key="index">
        <a :href="`https://api.themoviedb.org/movie/${movie.id}`">
          <img
            :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`"
            :alt="movie.original_title"
          />
        </a>
      </SwiperSlide>
      <div class="swiper-pagination"></div>
      <div class="swiper-button-next"></div>
      <div class="swiper-button-prev"></div>
    </Swiper>
  </div>
</template>
<script>
import {
  Navigation,
  Pagination,
  Scrollbar,
  A11y,
  Autoplay,
  EffectCoverflow,
} from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
// Import Swiper styles
import "swiper/css";
import "swiper/css/effect-coverflow";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";
export default {
  props: {
    movies: {
      type: Array,
      require: true,
    },
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [
        Navigation,
        Pagination,
        Scrollbar,
        A11y,
        Autoplay,
        EffectCoverflow,
      ],
    };
  },
};
</script>
<style lang="scss">
.movie__slider {
  width: 100%;
  margin-bottom: 100px;
  .Swiper {
    width: 100%;
    height: 100%; /* 높이를 100%로 설정하여 화면에 맞게 조정합니다 */
    padding: 20px 0 50px;
  }
}
</style>
