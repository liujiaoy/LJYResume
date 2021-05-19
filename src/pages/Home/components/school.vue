<template>
  <div class="education">
    <div class="school" v-for="item of baseInfo" :key="item.id">
      <svg class="icon" aria-hidden="true">
         <use :xlink:href="item.code"></use>
      </svg>
      <span class="key">{{item.key}}:</span>
      <span ref="what">{{item.value}}</span>
      <a v-if="item.src" :href="item.src" target="_blank">进入</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'School',
  data () {
    return {
      status: 'false',
      baseInfo: [
        {
          'id': '001',
          'key': '姓名',
          'value': '刘娇阳',
          'code': '#icongerenxinxi_baobeixingming'
        },
        {
          'id': '002',
          'key': '学校',
          'value': '江西理工大学',
          'code': '#iconxuexiao'
        },
        {
          'id': '003',
          'key': '专业',
          'value': '网络工程',
          'code': '#iconxuexiao1'
        },
        {
          'id': '004',
          'key': '籍贯',
          'value': '江西宜春',
          'code': '#iconjiguan'
        },
        {
          'id': '005',
          'key': '生日',
          'value': '1997.7',
          'code': '#iconDesert-'
        },
        {
          'id': '006',
          'key': '联系电话',
          'value': '157798870XX',
          'code': '#icondianhua'
        },
        {
          'id': '007',
          'key': '博客',
          'value': 'hexo/LJYALW',
          'src':'http://blog.better2020.top',
          'code': ''
        },
        {
          'id': '008',
          'key': 'GitHub',
          'src':'https://github.com/liujiaoy',
          'value': 'github.com/liujiaoy',
          'code': ''
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  span
    font-size: 1.5rem
  .education
    position: absolute
    left: 50%
    top: 4rem
    margin-left: -12rem
    .school
      margin-bottom: 2rem
      .key
        display: inline-block
        width: 10rem
    // .gitee
    //   position: absolute
    //   height: 5rem
    //   width: 10rem
    //   background: rgba(0,0,0,0.1)
</style>
