<template>
  <div style="width:100%">
    <div class="swiper-con">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(item ,index) in swiperAD" :key="index">
          <img :src="item"  style="width: 100%;height:100%"/>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Swiper from '../../../static/swiper'

export default {
  props: {
    swiperAD: {
      type: Array,
      default: []
    }
  },
  data() {
    return {
      
    }
  },
  created() {

  },
  updated() {
    var mySwiper = new Swiper('.swiper-con', {
      observer:true,//修改swiper自己或子元素时，自动初始化swiper 
      observeParents:true,//修改swiper的父元素时，自动初始化swiper 
      autoplay: true,
      speed: 800,
      loop: true,
      autoplayDisableOnInteraction : false
    })
  }
}
</script>
<style lang="stylus" scroped>
@import "../../common/stylus/mixin.styl";
.swiper-con
  width 375px
  height 160px
</style>
