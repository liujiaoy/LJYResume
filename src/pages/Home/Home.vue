<template>
  <div class="swiper">
    <swiper :options="swiperOption" class="swiper-content">
      <swiper-slide>
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
        on: {
          slideChangeTransitionStart: 'Test ()'
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        }
      }
    }
  },
  methods: {
    Test () {
      alert('1')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper
    position: relative
    height: 46rem
    background-color: rgba(124,205,124,0.3)
    overflow: hidden
    .swiper-container
      height: 100%
      width: 70%
      background-color: #fff
    .swiper-pagination
      position: absolute
      top: 0
      right: 2rem
      margin-top: 20rem
</style>
