<template>
<div>
  <div class="container">
    <LargeCardDisplay
    v-for="cardInfo in largeCardInfo"
    :key="cardInfo.id"
    :cardsSection="cardInfo"
    />

    <SmallCardDisplay
    v-for="cardInfo in smallCardInfo.slice(0,1)"
    :key="cardInfo.id"
    :cardsSection="cardInfo"

    />
  </div>
</div>
</template>

<script>
import {largeCardSections, smallCardSections} from "../../store/data";
export default {
  data(){
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>

<style  scoped>

</style>
