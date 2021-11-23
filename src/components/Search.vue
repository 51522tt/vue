<template>
    <div class='search'>
        <span class='iconfont'>&#xe62f;</span>
        <span class='search__defalutfont'>山姆会员商店优惠商品</span>
    </div>
</template>

<script>
export default {
  name: 'Search'
}
</script>

<style lang='scss' scoped>
@import '@/style/mixins.scss';

.search{
  background: #F5F5F5;
  border-radius: .16rem;
  color: #B7B7B7;
  padding-top:0.08rem;
  padding-bottom: 0.08rem;
  @include ellipsis;
  .iconfont{
    font-size: 0.16rem;
    margin-right: 0.12rem;
    margin-left:0.16rem
  }
  &__defalutfont{
    font-size: 0.14rem;
  }
}
</style>
