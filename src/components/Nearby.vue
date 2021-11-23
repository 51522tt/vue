<template>
  <div class="nearby">
    <h3 class="nearby__title">附近店铺</h3>
    <div class="nearby__item"
      v-for="(item,index) in nearbyList"
      :key="index"
    >
      <img
        :src="item.imgPath"
        class="nearby__item__img"
      />
      <div calss="nearby__content">
        <div class="nearby__content__title">{{item.title}}</div>
        <div class="nearby__content__tags">
          <span
            class="nearby__content__tag"
            v-for="(tag,index) in item.tags"
            :key="index"
            >{{tag}}</span>
        </div>
        <p class="nearby__content__highlight">
          {{item.highlight}}
        </p>
        <div class="nearby__content__hh"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Nearby',
  setup () {
    const nearbyList = [
      {
        imgPath: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送¥0', '基础运费¥5'],
        highlight: 'VIP尊享满89元减4元运费券（每月3张）'
      },
      {
        imgPath: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送¥0', '基础运费¥5'],
        highlight: 'VIP尊享满89元减4元运费券（每月3张）'
      },
      {
        imgPath: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送¥0', '基础运费¥5'],
        highlight: 'VIP尊享满89元减4元运费券（每月3张）'
      },
      {
        imgPath: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送¥0', '基础运费¥5'],
        highlight: 'VIP尊享满89元减4元运费券（每月3张）'
      },
      {
        imgPath: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送¥0', '基础运费¥5'],
        highlight: 'VIP尊享满89元减4元运费券（每月3张）'
      },
      {
        imgPath: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送¥0', '基础运费¥5'],
        highlight: 'VIP尊享满89元减4元运费券（每月3张）'
      }
    ]
    return { nearbyList }
  }
}
</script>

<style lang='scss' scoped>
.nearby {
  &__title {
    margin: 0.16rem 0 0.02rem 0;
    font-size: 0.18rem;
    font-weight: normal;
  }
  &__item {
    display: flex;
    padding-top: 0.12rem;
    // margin: 0.12rem 0;
    &__img {
      margin-right: 0.16rem;
      width: 0.56rem;
      height: 0.56rem;
    }
  }
  &__content {
    flex: 1;
    margin: 0.12rem 0;
    &__title {
      line-height: 0.22rem;
      font-size: 0.16rem;
    }
    &__tags {
      margin-top: 0.08rem;
      font-size: 0.13rem;
      line-height: 0.18rem;
    }
    &__tag {
      margin-right: 0.16rem;
    }
    &__highlight {
      margin: 0.08rem 0 0 0;
      color: #e93b3b;
      font-size: 0.13rem;
    }
    &__hh {
      padding-top: 0.12rem;
      width: 2.67rem;
      border-bottom: 0.01rem solid #f1f1f1;
    }
  }
}
</style>
