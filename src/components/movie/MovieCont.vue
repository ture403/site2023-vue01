<template>
  <div className="movie__cont container">
    <ul>
      <li v-for="(movie, index) in movies" :key="index">
        <a
          :href="`https://www.themoviedb.org/movie/${movie.id}`"
          target="_blank"
        >
          <img
            :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`"
            :alt="movie.title"
          />
          <em>
            <p className="title">{{ movie.title }}</p>
            <span className="star">{{ movie.vote_average }}</span>
          </em>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    movies: {
      type: Array,
      require: true,
    },
  },
};
</script>
<style lang="scss">
.movie__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    li {
      width: 23.333%;
      margin-bottom: 2%;
      margin-bottom: 10px;
      position: relative;
      .title {
        font-size: 20px;
        display: inline-block;
        padding: 3px 0;
        &:hover {
          text-decoration: underline;
          text-underline-position: under;
        }
      }
      .star {
        position: absolute;
        right: 20px;
        top: 20px;
        width: 30px;
        height: 30px;
        line-height: 30px;
        background-color: #fff;
        text-align: center;
        border-radius: 50%;
        font-size: 12px;
      }
    }
  }
}
</style>
