<template>
  <div>
    <div class="container">
      <hero-item />
      <large-card-display
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :card-section="cardInfo"
      />
      <small-card-display
        v-for="cardInfo in smallCardInfo"
        :key="cardInfo.id"
        :card-section="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '../assets/data.js'

export default {
  name: 'IndexPage',
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>
