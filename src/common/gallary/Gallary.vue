<template>
  <div class="container" @click="handleGallaryClick">
    <div class="wrapper">
      <swiper :options="swiperOption"  >
        <swiper-slide v-for="(item,index) in imgs" :key="index" >
          <img class="gallary-img"  :src="item" alt="">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CommonGallary',
  props: {
    imgs: {
      type: Array,
      default () {
        return ['https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1582908511716&di=feff50e32b89ee6c57e6cff6c1b3591f&imgtype=0&src=http%3A%2F%2Fimg3.duitang.com%2Fuploads%2Fitem%2F201608%2F17%2F20160817015723_UEKWM.thumb.700_0.jpeg',
          'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1582896679935&di=2b8dfa548bed4fac40bbb233f9b34630&imgtype=0&src=http%3A%2F%2Fcdn.duitang.com%2Fuploads%2Fitem%2F201410%2F21%2F20141021130151_ndsC4.jpeg'
        ]
      }
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observeParents: true,
        observer: true
      }
    }
  },
  methods: {
    handleGallaryClick () {
      this.$emit('close')
    }
  }
}
</script>
<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow : inherit
  .container
    display : flex
    flex-direction : column
    justify-content : center
    z-index : 99
    position : fixed
    left : 0
    right : 0
    top: 0
    bottom :0
    background :#000
    .wrapper
      width : 100%
      height : 0
      padding-bottom : 100%
      .gallary-img
        width: 100%
        height : 7.0rem
      .swiper-pagination
        color : #fff
        bottom : -1rem
</style>
