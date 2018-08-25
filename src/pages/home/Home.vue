<template>
  <div>
    <home-header></home-header>
    <carousel></carousel>
    <icons-area></icons-area>
    <recommend></recommend>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import Carousel from './components/Carousel'
import IconsArea from './components/IconsArea'
import Recommend from './components/Recommend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    Carousel,
    IconsArea,
    Recommend
  }
}
</script>
<style>

</style>
