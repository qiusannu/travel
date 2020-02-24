<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data: function () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/45/459bd3d00321a44790.water.jpg_200x200_6cd905a1.jpg',
        title: '景山公园',
        desc: '景山公园描述'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/9d/9d862d8166170089a3.img.jpg_200x200_8974965b.jpg',
        title: '北京园博园',
        desc: '北京园博园描述'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/07/a3231208ca4095bef77068c202d95bd2.jpg_200x200_0d7d4e22.jpg',
        title: '香山公园',
        desc: '香山公园描述'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/49/4982f8827fa2beacb4.water.jpg_200x200_647df78f.jpg',
        title: '大兴世界月季主题园',
        desc: '大兴世界月季主题园描述'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top .2rem
    line-height :.8rem
    background : #eee
    text-indent :.2rem
  .item
    display: flex
    height :1.9rem
    overflow : hidden
    .item-img
      width :1.7rem
      height : 1.7rem
      padding: .1rem
    .item-info
      flex :1
      padding : .1rem
      min-width :0
      .item-title
        line-height : .54rem
        font-size : .32rem
        ellipse()
      .item-desc
        line-height : .4rem
        color: #ccc
        ellipse()
      .item-button
        margin-top : .1rem
        background : #ff9300
        padding : 0.05rem 0.2rem
        font-size : .25rem
        border-radius : .06rem
        color : #fff
</style>
