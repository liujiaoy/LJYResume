<template>
  <div class="swiper">
    <swiper :options="swiperOption" class="swiper-content">
      <swiper-slide >
        <base-info></base-info>
      </swiper-slide>
      <swiper-slide>
        <school></school>
      </swiper-slide>
      <swiper-slide>
        <project-one></project-one>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
import BaseInfo from './components/base-info'
import School from './components/school'
import ProjectOne from './components/project-one'
export default {
  name: 'Home',
  components: {
    BaseInfo,
    School,
    ProjectOne
  },
  data () {
    return {
      swiperOption: {
        direction: 'vertical',
        speed: 1000,
        slidesPerView: 1,
        spaceBetween: 100,
        mousewheel: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },
        height:document.documentElement.clientHeight
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper
    position: relative
    background-color: rgba(124,205,124,0.3)
    .swiper-container
      height: 100%
      width: 70%
      background-color: #fff
    .swiper-pagination
      position: absolute
      top: 0
      right: 2rem
      margin-top: 20rem
  @media screen and (max-width:720px)
    .swiper
      position: relative
      background-color: rgba(124,205,124,0.3)
      overflow: auto
      .swiper-container
        height: 100%
        width: 100%
        background-color: #fff
  
</style>
