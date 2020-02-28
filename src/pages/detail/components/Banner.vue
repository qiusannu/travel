<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="" alt="">
      <div class="banner-info">
        <div class="banner-title">大连圣亚海洋世界(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe612;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose">

    </common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: [
        'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1582908511716&di=feff50e32b89ee6c57e6cff6c1b3591f&imgtype=0&src=http%3A%2F%2Fimg3.duitang.com%2Fuploads%2Fitem%2F201608%2F17%2F20160817015723_UEKWM.thumb.700_0.jpeg',
        'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1582896679935&di=2b8dfa548bed4fac40bbb233f9b34630&imgtype=0&src=http%3A%2F%2Fcdn.duitang.com%2Fuploads%2Fitem%2F201410%2F21%2F20141021130151_ndsC4.jpeg'
      ]
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>
<style lang="stylus" scoped>
  .banner
    position : relative
    overflow : hidden
    height : 0
    background : #555
    padding-bottom: 55%
    .banner-img
      width:100%
    .banner-info
      display : flex
      position : absolute
      left : 0
      right : 0
      bottom : 0
      line-height: .6rem;
      color : #fff
      background-image : linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title
        flex: 1;
        font-size : .32rem
        padding : 0 .2rem
      .banner-number
        margin-top : 0.14rem
        padding : 0 .4rem
        line-height : .32rem
        height : .32rem
        font-size .24rem
        border-radius : .2rem
        background : rgba(0,0,0,0.8)
</style>
