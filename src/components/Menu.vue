<template>
  <div class="docker">
      <!-- BEM 命名规则 元素 —— 状态 -- -->
      <div
        v-for='(item,index) in menuList'
        :key = "item.icon"
        :class="{'docker__item':true,'docker__item--active':index===0}"
        >
          <div class="iconfont" v-html='item.icon'/>
          <div class="docker__title">{{item.text}}</div>
    </div>
      <n-card>
      <template #header>
        <n-skeleton text v-if="loading" width="60%" />
        <template v-else>I'm OK</template>
      </template>
      <n-skeleton text v-if="loading" :repeat="6" />
      <template v-else>
        不要忘了留姓名<br />
        电话和其他事情<br />
        不要说的太快免得我没写下你大名<br />
        或许你不再打来<br />
        我却等到头发白<br />
        希望有一天你会打来
      </template>
    </n-card>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  setup () {
    const menuList = [
      { icon: '&#xe6b8;', text: '首页' },
      { icon: '&#xe600;', text: '购物车' },
      { icon: '&#xe7b3;', text: '订单' },
      { icon: '&#xe78b;', text: '我的' }
    ]
    return { menuList }
  }
}
</script>

<style lang="scss" scoped>
.docker{
    display: flex;
    box-sizing:border-box;
    padding:0 0.18rem;
    &__item{
        flex: 1;
        text-align: center;
        .iconfont {
            margin: 0.07rem 0 0.02rem 0;
        }
        &--active {
            color: #1FA4FC;
        }
    };
    &__title {
        font-size:.2rem;
        /* 浏览器默认最小元素12 px */
        transform: scale(.5, .5);
        transform-origin: center top;
    }
}
</style>
