<template>
  <div>
    <div>
      <Nav />
    </div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="{ title, snippet, cards, id } in largeCardInfo"
        :key="id"
        :title="title"
        :snippet="snippet"
        :cards="cards"
      />
      <SmallCardDisplay
        v-for="{ id, title, cards } in smallCardInfo"
        :key="id"
        :title="title"
        :images="cards"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '../data.js'
export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    }
  },
}
</script>
