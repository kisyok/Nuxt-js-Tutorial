<template>
  <div>
    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo.slice(0,1)"
        :key="cardInfo.id"
        :card-section="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardInfo"
        :key="cardInfo.id"
        :card-section="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>
