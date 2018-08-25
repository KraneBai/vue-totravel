<template>
  <div class="recommend">
    <div class="rec-tit">热销推荐</div>
    <ul>
      <li class="rec-item border-bottom" v-for="item of itemList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      itemList: [
        {
          id: '001',
          title: '【国庆预售】北京出发西藏拉萨+布达拉宫+雅鲁藏布大峡谷+鲁朗林海+南伊沟+羊湖+纳木措双卧12或卧飞10日游',
          desc: '(300多人销量+第二人立减200元优惠+北京成团+全程升级挂三星住宿)',
          imgUrl: 'https://b2-q.mafengwo.net/s11/M00/F4/F4/wKgBEFrRzFKAZXxHAEHCyNlvgPQ075.gif?imageMogr2%2Fthumbnail%2F%21440x270r%2Fgravity%2FCenter%2Fcrop%2F%21440x270%2Fquality%2F90'
        },
        {
          id: '002',
          title: '【【歌诗达大西洋号】深圳往返日本6天5晚邮轮之旅',
          desc: '（免签证+含港务税费+同舱第三四人免船票+标价为优惠后均价）',
          imgUrl: 'https://n1-q.mafengwo.net/s11/M00/65/78/wKgBEFqw5q-ACORhAALWXxeqdaw970.gif?imageMogr2%2Fthumbnail%2F%21440x270r%2Fgravity%2FCenter%2Fcrop%2F%21440x270%2Fquality%2F90'
        },
        {
          id: '003',
          title: '【[北京送签]日本单次旅游签证',
          desc: '（免机酒+可简化+可加急+2人立减优惠+拒签双倍退+顺丰包邮+一手送签社+诚信经营无套路）',
          imgUrl: 'https://p1-q.mafengwo.net/s11/M00/7F/57/wKgBEFsUwtyAaMoaAALst-d5xH4372.gif?imageMogr2%2Fthumbnail%2F%21440x270r%2Fgravity%2FCenter%2Fcrop%2F%21440x270%2Fquality%2F90'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixin.styl'
.rec-tit
  background #eee
  margin-top .2rem
  line-height .8rem
  text-indent .2rem
.rec-item
  overflow hidden
  display flex
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex 1
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-btn
      background #ff9300
      padding 0 .2rem
      margin-top .16rem
      color #fff
      border-radius .06rem
      line-height .44rem
</style>
