<template>
  <div class="articles">
    <div class="art-tit">热门游记</div>
    <ul>
      <li class="border-bottom" v-for="item of itemList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeArticles',
  data () {
    return {
      itemList: [
        {
          id: '001',
          title: '去济州岛结果天天下雨怎么办那只能吃回来了',
          desc: ' 先来一波小姐姐的照片？ 看看这狗封面，再看看以前的游记封面就知道，这回啥好看的照片都没有拍到 这个标题其实已经就涵盖了本次旅游的全部内容了。在6月28日到了 济州岛 的那一天开始，我',
          imgUrl: 'http://b4-q.mafengwo.net/s11/M00/0F/4A/wKgBEFtGEr6AJ1RfABSI2AL7rtQ44.jpeg?imageMogr2%2Fthumbnail%2F%21440x300r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21440x300%2Fquality%2F90'
        },
        {
          id: '002',
          title: '不去泰姬陵，北印还能怎么玩？斋浦尔（粉红之城）+新德里',
          desc: ' 印度之行，了解了啥？ 斋浦尔-尼桑木丁圣陵：亲身体验了《小萝莉的神猴大叔》那种宗教唱诗仪式！ 虽然狂热的宗教仪式对异教徒而言是恐怖的，但原汁原味仍强烈推荐这里。 斋浦尔-琥珀堡：坐',
          imgUrl: 'http://b2-q.mafengwo.net/s11/M00/B5/FE/wKgBEFs8i_qAJWh7AB4NfjTHSQ843.jpeg?imageMogr2%2Fthumbnail%2F%21440x300r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21440x300%2Fquality%2F90'
        },
        {
          id: '003',
          title: '南极，漫漫旅途的终点，行程全记录。',
          desc: '（ 今年伊始，有一波南极游记狂潮席卷整个网络。半年过去，南极话题终于凉了下来。在 福州 狗都愿意憋着尿不出门的最炎热的时候，聊聊我的南极行始末。 去年我有一个自己看来宏大的计划，从 美',
          imgUrl: 'http://n3-q.mafengwo.net/s11/M00/07/53/wKgBEFszcJyAKQ6cAAGgBUAHr-855.jpeg?imageMogr2%2Fthumbnail%2F%21440x300r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21440x300%2Fquality%2F90'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixin.styl'
.art-tit
  background #eee
  margin-top .2rem
  line-height .8rem
  text-indent .2rem
.item-img-wrapper
  overflow hidden
  height 0
  padding-bottom 33.9%
  img
    width 100%
.item-info
  padding .1rem
  .item-title
    line-height .54rem
    font-size .32rem
    ellipsis()
  .item-desc
    line-height .4rem
    color #ccc
    ellipsis()
</style>
