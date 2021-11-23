<template>
  <div class="features">
    <span class="features__item"
     v-for='(item,index) in featureList'
     :key="index"
      >
      <img
        class="features__item__defalutimg"
        :src="item.imgPath"
        alt=""
      />
      <div class="features__item__defalutfont">{{item.titel}}</div>
    </span>
  </div>
</template>

<script>
export default {
  name: 'Features',
  setup () {
    const featureList = [
      {
        titel: '超市便利',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/超市.png'
      },
      {
        titel: '菜市场',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/菜市场.png'
      },
      {
        titel: '水果店',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/水果店.png'
      },
      {
        titel: '鲜花绿植',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/鲜花.png'
      },
      {
        titel: '医药健康',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/医药健康.png'
      },
      {
        titel: '家具时尚',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/家居.png'
      },
      {
        titel: '烘培蛋糕',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/蛋糕.png'
      },
      { titel: '签到', imgPath: 'http://www.dell-lee.com/imgs/vue3/签到.png' },
      {
        titel: '大牌免运',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/大牌免运.png'
      },
      {
        titel: '红包套餐',
        imgPath: 'http://www.dell-lee.com/imgs/vue3/红包.png'
      }
    ]
    return { featureList }
  }
}
</script>

<style lang='scss' scoped>
.features {
  display: flex;
  flex-wrap: wrap;
  box-sizing: border-box;
  &__item {
    // flex: 1;
    text-align: center;
    width: 20%;
    margin-bottom: 0.16rem;
    &__defalutimg {
      display: block;
      margin: 0 auto;
      width: 0.4rem;
      height: 0.4rem;
      margin-bottom: 0.06rem;
    }
  }
}
</style>
