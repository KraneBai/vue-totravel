<template>
  <div>
    <home-header></home-header>
    <carousel></carousel>
    <icons-area></icons-area>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import Carousel from './components/Carousel'
import IconsArea from './components/IconsArea'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    Carousel,
    IconsArea
  }
}
</script>
<style>

</style>
