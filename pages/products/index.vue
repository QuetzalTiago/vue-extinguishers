<template>
  <div>
    <div class="container">
      <LargeCardDisplay
        v-for="{ id, title, snippet, cards } in largeCardInfo.slice(0, 1)"
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
import { largeCardSections, smallCardSections } from '../../data.js'

export default {
  data: () => ({
    largeCardInfo: largeCardSections,
    smallCardInfo: smallCardSections,
  }),
}
</script>

<style scoped></style>
