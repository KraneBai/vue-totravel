<template>
  <div>
    <home-header></home-header>
    <carousel></carousel>
    <icons-area></icons-area>
    <recommend></recommend>
    <articles></articles>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import Carousel from './components/Carousel'
import IconsArea from './components/IconsArea'
import Recommend from './components/Recommend'
import Articles from './components/Articles'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    Carousel,
    IconsArea,
    Recommend,
    Articles
  }
}
</script>
<style>

</style>
