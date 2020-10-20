<template>
  <div class="bg">
    <div class="photo">
      <img class="img" src="../../../assets/yierkanhua.png" />
    </div>
    <div class="name">{{name}}</div>
    <div class="welcome animated bounce">{{welcome}}</div>
  </div>
</template>

<script>
export default {
  name: 'BaseInfo',
  data () {
    return {
      name: '你也来看fafa吗',
      welcome: '种花007号已就位'
    }
  },
  mounted () {
    console.log('mounted')
  },
  activated () {
    console.log('aaa')
  }
}
</script>

<style lang="stylus" scoped>
  .bg
    display: flex
    flex-direction: column
    align-items: center
    font-family: "comic sans ms"
    .photo
      margin-top: 10rem
      margin-bottom: 2rem
      height: 10rem
      width: 10rem
      background: #fff
      border-radius: 25%
      overflow: hidden
      .img
        width: 100%
    .name
      height: 2rem
      width: 10rem
      line-height: 2rem
      text-align: center
      font-size: 1.2rem
      font-family: "comic sans ms"
      border-radius: .4rem
    .welcome
      position: absolute
      bottom: 2rem
</style>
