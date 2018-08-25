<template>
  <div class="detail">
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :detailList="detailList"></detail-list>
    </div>
  </div>
</template>
<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      detailList: [{
        title: '促销票',
        children: [{
          title: '项目1',
          children: [{
            title: '第三列'
          }, {
            title: '第三列2'
          }]
        }, {
          title: '项目2'
        }]
      }, {
        title: '成人票'
      }, {
        title: '学生票'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
.content
  height 50rem
</style>
