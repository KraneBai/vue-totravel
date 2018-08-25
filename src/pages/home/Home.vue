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
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeCarousel,
    HomeIconsArea,
    HomeRecommend,
    HomeArticles
  },
  mounted () {
    this.getHomeInfo()
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      console.log(res)
    }
  }
}
</script>
<style>

</style>
