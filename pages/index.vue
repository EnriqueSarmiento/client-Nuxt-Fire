<template>
<div>
  <Nav/>
  <div class="container">
    <Hero/>
    <div class="margen-idk">
      <br>
    </div>
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    <SmallCardDisplay
    v-for="cardInfo in smallCardInfo"
    :key="cardInfo.id"
    :cardsSection="cardInfo"
    />

  </div>
</div>
</template>

<script>
import { largeCardSections } from "../store/data";
import { smallCardSections } from "../store/data";
export default {
  name: 'IndexPage',
  data(){
    return{
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>

<style scoped>
  .margen-idk{
    margin-top: 10rem;
    height: 1px;
  }
</style>>

