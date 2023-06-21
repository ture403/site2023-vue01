<template>
  <div className="Unsplash__cont container">
    <ul>
      <li v-for="(unsplash, index) in unsplashs" :key="index">
        <a
          :href="`https://unsplash.com/search/photos/${unsplash.id}`"
          target="_blank"
        >
          <img :src="unsplash.urls.regular" :alt="unsplash.alt_description" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    unsplashs: {
      type: Array,
      require: true,
    },
  },
};
</script>
<style lang="scss">
.Unsplash__cont {
  ul {
    column-count: 3;

    li {
      margin-bottom: 10px;
    }
  }
}
</style>
