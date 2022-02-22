<template>
  <div class="one">
    <div class="name">Vue仿去哪儿网</div>
    <div class="content">
      <swiper :options="swiperOption">
        <swiper-slide
          v-for="item of imgList"
          :key="item.id"
        >
          <img
            class="img-item"
            :src="item.imgUrl"  />
        </swiper-slide>
      </swiper>
    </div>
    <div class="play">
      <a target="_blank" href="http://travel.better2020.top/dist">进去瞅瞅</a>
    </div>
  </div>
</template>
<script>
export default {
  name: 'ProjectOne',
  data () {
    return {
      swiperOption: {
        effect: 'cube',
        grabCursor: true,
        autoplay: true,
        loop: true,
        speed: 1000,
        cubeEffect: {
          shadow: true,
          slideShadows: true,
          shadowOffset: 20,
          shadowScale: 0.94
        },
        pagination: {
          el: '.swiper-pagination'
        }
      },
      imgList: [
        {
          id: '001',
          imgUrl: '/static/img/swiper1.png'
        }, {
          id: '002',
          imgUrl: '/static/img/swiper2.png'
        }, {
          id: '003',
          imgUrl: '/static/img/swiper3.png'
        }, {
          id: '004',
          imgUrl: '/static/img/swiper4.png'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .one
    .name
      height: 10rem
      background: #42B983
      line-height: 10rem
      text-align: center
      font-size: 2rem
    .content
      .swiper-container
        width: 20rem!important
        height: 20rem
        position: absolute
        left: 50%
        top: 55%
        margin-left: -10rem
        margin-top: -10rem
      .swiper-slide
        background-position: center
        background-size: cover
        background: rgba(67,205,128,0.7)
        .img-item
          width: 100%
          height: 100%
    .play
      position: absolute
      left: 50%
      bottom: 4rem
      margin: 0 auto
      a:visited
        color: #000
      a:hover
        color: #42B983
        text-decoration:none
</style>
