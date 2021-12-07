<template>
  <NuxtLink :to="`/products/${id}`" class="card-container">
    <img :src="image" alt="" class="image" />
  </NuxtLink>
</template>

<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: ['image', 'id'],
}
</script>

<style scoped>
.card-container {
  width: 24%;
  height: 12.5rem;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  cursor: pointer;
}
.image {
  width: 100%;
  height: 100%;
}
</style>
