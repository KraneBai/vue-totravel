<template>
  <div>
    <home-header></home-header>
    <carousel></carousel>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import Carousel from './components/Carousel'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    Carousel
  }
}
</script>
<style>

</style>
