<template>
  <NuxtLink :to="`products/${id}`" class="card">
    <img :src="image" alt="" class="image" />
    <h3 class="header">{{ title }}</h3>
    <p class="snippet">{{ snippet }}</p>
  </NuxtLink>
</template>

<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: ['image', 'title', 'snippet', 'id'],
}
</script>

<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
.snippet {
  color: grey;
}
</style>
