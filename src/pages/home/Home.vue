<template>
  <div>
    <home-header></home-header>
    <home-carousel></home-carousel>
    <home-icons-area></home-icons-area>
    <home-recommend></home-recommend>
    <home-articles></home-articles>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeCarousel from './components/Carousel'
import HomeIconsArea from './components/IconsArea'
import HomeRecommend from './components/Recommend'
import HomeArticles from './components/Articles'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeCarousel,
    HomeIconsArea,
    HomeRecommend,
    HomeArticles
  }
}
</script>
<style>

</style>
