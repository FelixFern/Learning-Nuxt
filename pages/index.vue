<template>
  <div>
    <Hero />
    <Large-card-display 
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardSection="cardInfo"
    />
    <Small-card-display 
      v-for="cardInfo in smallCardInfo"
      :key="cardInfo.id"
      :cardSection="cardInfo"
    />
  </div>
  
</template>

<script>
  import { largeCardSections, smallCardSections } from "@/static/data.js"
    export default {
        data() {
            return {
              largeCardInfo: largeCardSections,
              smallCardInfo: smallCardSections
            }
        }
    }
</script>
