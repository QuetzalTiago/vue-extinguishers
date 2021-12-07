<template>
  <div class="container">
    <h4 class="header">{{ title }}</h4>
    <div class="card-container">
      <SmallCard
        v-for="{ id, image } in images"
        :id="id"
        :key="id"
        :image="image"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'images'],
}
</script>

<style scoped>
.container {
  padding: 2rem 0;
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}
.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
