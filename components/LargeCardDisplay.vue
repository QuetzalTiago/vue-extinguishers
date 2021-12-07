<template>
  <div class="container">
    <h4 class="header">{{ title }}</h4>
    <p class="snippet">
      {{ snippet }}
    </p>
    <div class="cards-container">
      <LargeCard
        v-for="{ id, title, image, snippet } in cards"
        :id="id"
        :key="id"
        :title="title"
        :image="image"
        :snippet="snippet"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'snippet', 'cards'],
}
</script>

<style scoped>
.container {
  margin-top: 2rem;
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
}
.snippet {
  color: grey;
  margin-bottom: 1.5rem;
}
.cards-container {
  display: flex;
  justify-content: space-between;
}
</style>
