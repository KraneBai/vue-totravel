<template>
  <div id="app">
    <!-- Detail页面不被缓存 -->
    <!-- <keep-alive exclude="Detail"> -->
    <keep-alive>
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style></style>
