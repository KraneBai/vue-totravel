<template>
  <div>
    <home-header :city="city"></home-header>
    <home-carousel :swiper="swiperList"></home-carousel>
    <home-icons-area :icons="iconList"></home-icons-area>
    <home-recommend :recommend="recommendList"></home-recommend>
    <home-articles :articles="articlesList"></home-articles>
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
  data () {
    return {
      city: '',
      swiperList: [],
      recommendList: [],
      articlesList: [],
      iconList: []
    }
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
      if (res.data.ret && res.data.data) {
        const data = res.data.data
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.articlesList = data.articlesList
      }
    }
  }
}
</script>
<style>

</style>
